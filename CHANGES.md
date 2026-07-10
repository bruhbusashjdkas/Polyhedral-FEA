# CHANGES.md — How to send code without wrecking the repo

You are new to git. That is fine. **Read this whole file. Follow every checklist. Do not improvise.**

Paste this file into your AI agent. Agents must obey it.

Default branch: **`master`**.
Remote: `https://github.com/Hunter-124/Polyhedral-FEA`

---

## 1. Golden rules (absolute)

1. **Never** force-push `master`. Ever.
2. **Never** run `git push --force` / `git push -f` unless the owner told you to, on **your** branch only.
3. **Never** commit secrets (API keys, tokens, `.env`, passwords, private keys).
4. **Never** commit `build/`, object files, or generated binaries.
5. **Never** amend or rewrite history that is already on GitHub unless the owner says so.
6. **Never** skip the build or tests.
7. **Never** “fix” tests by hardcoding expected answers in `src/`. That is cheating. PR will be rejected.
8. **Never** put `Co-Authored-By`, “Generated with Claude/Grok/Cursor”, or any AI attribution in commits, PRs, or messages.
9. One logical change per PR. Not ten features dumped together.
10. Branch names: `yourname/short-topic` (e.g. `alex/fix-hex-jacobian`). No spaces.
11. You own clean merges. If your branch conflicts with `master`, **you** fix it before asking for review.
12. Use **your** git name/email. Do not pretend to be Hunter-124.

---

## 2. First-time machine setup

### Install git

**Fedora / RHEL:**
```bash
sudo dnf install -y git
```

**Debian / Ubuntu:**
```bash
sudo apt-get update && sudo apt-get install -y git
```

**macOS:**
```bash
xcode-select --install
```

### Clone and enter the repo
```bash
git clone https://github.com/Hunter-124/Polyhedral-FEA.git
cd Polyhedral-FEA
git checkout master
git pull origin master
```

### Set who you are (use YOUR real identity)
```bash
git config user.name "YOUR NAME"
git config user.email "YOUR_EMAIL@example.com"
```

Check:
```bash
git config user.name
git config user.email
```

### Optional: GitHub CLI
```bash
# Fedora:
sudo dnf install -y gh
# then:
gh auth login
```

---

## 3. Every time you start work

Do this **before** editing anything:

```bash
cd Polyhedral-FEA
git checkout master
git pull origin master
git status
```

`git status` must show a clean tree (no leftover junk from last time).

Create your branch **from** up-to-date `master`:
```bash
git checkout -b yourname/short-topic
git status
```

You should be on `yourname/short-topic`, not `master`.

---

## 4. While working

### See what changed
```bash
git status
git diff
```

### Stage files (do NOT blind-add everything)
```bash
# GOOD — name the files
git add path/to/file1.cpp path/to/file1.hpp

# BAD — dumps trash into the commit
git add .
git add -A
```

Only stage source you meant to change. **Never** stage:
- `build/`
- secrets / `.env` / key files
- random binaries, screenshots dumps, editor swap files

### Commit
```bash
git commit -m "Fix hex Jacobian sign on inverted corners"
```

Message rules:
- Imperative mood: “Fix …”, “Add …”, “Remove …”
- Say **what** and **why**, not “updates” or “wip”
- One logical change per commit when possible

**Ask first** before committing LICENSE rewrites or huge binary blobs.

### Still dirty? Keep going
```bash
git status
git diff
# edit more…
git add the/files/you/touched
git commit -m "Another clear message"
```

---

## 5. Before you say “done” (mandatory gate)

**If any step fails, you are not done.**

### C++ style (if you touched C++)
```bash
# Format the files you changed, e.g.:
clang-format -i path/to/file.cpp path/to/file.hpp
```

### Build + tests (repo root as CWD)
```bash
cd /path/to/Polyhedral-FEA
cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug
cmake --build build && ctest --test-dir build
```

Both must succeed. No red tests. No “it works on my machine” excuses.

### Final scrub
- [ ] No leftover `std::cout` / debug spam you meant to remove
- [ ] No secrets in the diff
- [ ] No `build/` files staged
- [ ] `git status` only shows what belongs in the PR

```bash
git status
git diff master...HEAD
```

---

## 6. Ship your change

### If you have write access to the repo
```bash
git push -u origin yourname/short-topic
```

Open a PR **into `master`**:
```bash
gh pr create --base master --head yourname/short-topic --title "Short clear title" --body "What changed and why. How you tested."
```

Or open the compare URL Git prints after push and use the GitHub UI.

- Wait for CI.
- Fix failures on **your branch**. Do not spam empty commits.
- Do not merge to `master` yourself during day-one (see §10).

### If you do **not** have write access (fork workflow)
```bash
# On GitHub: click Fork on Hunter-124/Polyhedral-FEA, then:
git clone https://github.com/YOUR_GITHUB_USERNAME/Polyhedral-FEA.git
cd Polyhedral-FEA
git remote add upstream https://github.com/Hunter-124/Polyhedral-FEA.git
git checkout master
git pull upstream master
git checkout -b yourname/short-topic
# … work, commit, pass §5 gate …
git push -u origin yourname/short-topic
```

Open a PR from **your fork’s branch** → **`Hunter-124/Polyhedral-FEA` `master`**.

Keep your fork’s `master` updated:
```bash
git checkout master
git pull upstream master
git push origin master
```

---

## 7. If you broke something

| Situation | Command | Notes |
|-----------|---------|--------|
| Unstage a file | `git restore --staged path/to/file` | File stays on disk |
| Discard edits to a tracked file | `git restore path/to/file` | **Deletes your edits** in that file |
| Remove an untracked file | `git clean -n` then `git clean -f path` | Always dry-run (`-n`) first |
| Undo last commit, keep changes | `git reset --soft HEAD~1` | Safe if not pushed |
| Undo last commit, drop changes | `git reset --hard HEAD~1` | **DESTROYS WORK. Double-check.** |

**HARD reset rules:**
- `git reset --hard` **destroys uncommitted work**. There is often no undo.
- **Never** `git reset --hard` on `master` or any branch others use.
- **Never** hard-reset then force-push a shared branch.

Already pushed a bad commit on **your** private branch? Prefer a new fixing commit. Do not rewrite published history unless the owner says so.

---

## 8. Forbidden (do these and your PR dies)

| Forbidden | Why |
|-----------|-----|
| Force-push `master` | Breaks everyone |
| `git push --force` without owner OK | Rewrites shared history |
| Delete remote branches you did not create | Not your branch |
| Rewrite `master` history | Absolute ban |
| Commit `build/` or binaries | Repo bloat, fights |
| Commit API keys / secrets | Security incident |
| Hardcode benchmark answers in `src/` | Cheating |
| Skip cmake/ctest | Broken code lands |
| Mix 10 unrelated features in one PR | Unreviewable |
| AI attribution in commits/PRs | Against project policy |
| Commit as Hunter-124 when you are not | Identity fraud |

---

## 9. Agent prompt template

Copy-paste to your AI agent:

```text
Read CHANGES.md and CONTRIBUTING.md in this repo and follow them exactly.

Work only on branch: yourname/short-topic
Base all work on up-to-date master. Do not commit to master.

Mandatory gates before claiming done:
- clang-format on touched C++ files
- cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug
- cmake --build build && ctest --test-dir build (from repo root)
- clean git status; no secrets; no build/ artifacts

Rules:
- Do not force-push. Do not rewrite published history.
- Stage specific files only (no blind git add .).
- Commit messages: imperative, clear why.
- Commit as me (my git user.name / user.email). Never as Hunter-124 unless I am Hunter-124.
- Never add Co-Authored-By, "Generated with …", or any AI attribution to commits or PRs.
- One logical change. Do not hardcode test answers in src/.
- I own merge conflicts; help me fix them on my branch.
```

---

## 10. Owner / master policy

- **Only Hunter-124** (or the owner’s agents) merges to `master` during day-one.
- Friends: open PRs. Wait. Do not merge your own PR into `master` unless the owner says so.
- Day-one work by the owner may land straight on `master`. That does **not** give you the same privilege.
- License: **BSD-3-Clause**. Do not rewrite the LICENSE.

---

## Quick checklist (print this)

- [ ] `git pull` on `master` before branching
- [ ] Branch named `yourname/short-topic`
- [ ] Only intended files staged
- [ ] No secrets, no `build/`
- [ ] clang-format (C++ touches)
- [ ] `cmake --build build && ctest --test-dir build` green
- [ ] Clear commit messages, no AI attribution
- [ ] Pushed branch, PR into `master`
- [ ] CI green; conflicts fixed by **you**

If you skip a box, you are not ready.
