# Graph Report - .  (2026-07-10)

## Corpus Check
- Corpus is ~35,673 words - fits in a single context window. You may not need a graph.

## Summary
- 597 nodes · 1084 edges · 27 communities (24 shown, 3 thin omitted)
- Extraction: 83% EXTRACTED · 17% INFERRED · 0% AMBIGUOUS · INFERRED: 181 edges (avg confidence: 0.63)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]
- [[_COMMUNITY_Community 5|Community 5]]
- [[_COMMUNITY_Community 6|Community 6]]
- [[_COMMUNITY_Community 7|Community 7]]
- [[_COMMUNITY_Community 8|Community 8]]
- [[_COMMUNITY_Community 9|Community 9]]
- [[_COMMUNITY_Community 10|Community 10]]
- [[_COMMUNITY_Community 11|Community 11]]
- [[_COMMUNITY_Community 12|Community 12]]
- [[_COMMUNITY_Community 13|Community 13]]
- [[_COMMUNITY_Community 14|Community 14]]
- [[_COMMUNITY_Community 15|Community 15]]
- [[_COMMUNITY_Community 16|Community 16]]
- [[_COMMUNITY_Community 17|Community 17]]
- [[_COMMUNITY_Community 18|Community 18]]
- [[_COMMUNITY_Community 19|Community 19]]
- [[_COMMUNITY_Community 20|Community 20]]
- [[_COMMUNITY_Community 21|Community 21]]
- [[_COMMUNITY_Community 22|Community 22]]
- [[_COMMUNITY_Community 23|Community 23]]
- [[_COMMUNITY_Community 24|Community 24]]
- [[_COMMUNITY_Community 25|Community 25]]
- [[_COMMUNITY_Community 26|Community 26]]

## God Nodes (most connected - your core abstractions)
1. `Viewport` - 43 edges
2. `Palette` - 36 edges
3. `NodalMesh` - 29 edges
4. `App` - 27 edges
5. `src/mesh` - 21 edges
6. `Material` - 20 edges
7. `Model` - 19 edges
8. `SolveResult` - 19 edges
9. `src/fea` - 19 edges
10. `SolveJob` - 18 edges

## Surprising Connections (you probably didn't know these)
- `assemble_body_load()` --calls--> `body_force`  [INFERRED]
  src/fea/src/assembly.cpp → tests/support/mms.hpp
- `single_element()` --calls--> `reference_nodes()`  [INFERRED]
  tests/test_tier0.cpp → src/fea/src/shape.cpp
- `solve_scf()` --calls--> `recover_nodal_stress()`  [INFERRED]
  tests/test_goodier_cavity.cpp → src/fea/src/stress.cpp
- `solve_l()` --calls--> `recover_nodal_stress()`  [INFERRED]
  tests/test_l_domain.cpp → src/fea/src/stress.cpp
- `solve_l()` --calls--> `assemble_traction_load()`  [INFERRED]
  tests/test_l_domain.cpp → src/fea/src/traction.cpp

## Import Cycles
- None detected.

## Communities (27 total, 3 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.05
Nodes (62): BodyForce, Index, MatrixXd, SparseMatrix, element_num_nodes(), ElementType, uint32_t, vector (+54 more)

### Community 1 - "Community 1"
Cohesion: 0.07
Nodes (33): array, Element, num_nodes, order, stiffness, Material, d_matrix, poissons_ratio (+25 more)

### Community 2 - "Community 2"
Cohesion: 0.08
Nodes (26): vector, Matrix3d, BenchError, map, string, ReferenceCase, citation, name (+18 more)

### Community 3 - "Community 3"
Cohesion: 0.09
Nodes (38): App, deform_scale, hovered_region, job, load_force, mode, model, open_path (+30 more)

### Community 4 - "Community 4"
Cohesion: 0.06
Nodes (36): ImVec4, Palette, accent, accent_dim, accent_mid, accent_soft, accent_soft_top, axis_x (+28 more)

### Community 5 - "Community 5"
Cohesion: 0.17
Nodes (36): audit, loop, ci, CHANGES.md — How to send code without wrecking the repo, SPDX-License-Identifier: BSD-3-Clause, CONTRIBUTING — Codebase map & standards, PolyMesh, SPDX-License-Identifier: BSD-3-Clause (+28 more)

### Community 6 - "Community 6"
Cohesion: 0.10
Nodes (26): Soup, GeomError, array, uint32_t, vector, Vector3d, TriSurface, triangles (+18 more)

### Community 7 - "Community 7"
Cohesion: 0.07
Nodes (30): DisplayMode, uint32_t, Vector3d, VectorXd, Viewport, background_program_, background_vao_, baked_max_ (+22 more)

### Community 8 - "Community 8"
Cohesion: 0.13
Nodes (27): GmshType, map, string, vector, MshModel, mesh, physical_faces, physical_names (+19 more)

### Community 9 - "Community 9"
Cohesion: 0.12
Nodes (21): Vector3d, QuadraturePoint, weight, xi, ElementType, span, vector, default_rule() (+13 more)

### Community 10 - "Community 10"
Cohesion: 0.13
Nodes (24): face_num_nodes(), FaceType, uint32_t, vector, SurfaceFace, nodes, type, assemble_traction_load() (+16 more)

### Community 11 - "Community 11"
Cohesion: 0.11
Nodes (21): CellId, CellKind, FaceId, runtime_error, Cell, faces, kind, Face (+13 more)

### Community 12 - "Community 12"
Cohesion: 0.19
Nodes (19): Dynamic, Matrix, VectorXd, ShapeEval, dn, n, ElementType, vector (+11 more)

### Community 13 - "Community 13"
Cohesion: 0.12
Nodes (19): set_result, array, map, uint32_t, vector, VectorXd, SolveResult, boundary_quads (+11 more)

### Community 14 - "Community 14"
Cohesion: 0.16
Nodes (8): run(), apply_theme(), atomic, mutex, optional, path, write_box_stl(), thread

### Community 15 - "Community 15"
Cohesion: 0.17
Nodes (14): cells, set_status, optional, size_t, string, Vector3d, Model::load(), point_triangle_distance() (+6 more)

### Community 16 - "Community 16"
Cohesion: 0.21
Nodes (14): Camera, distance_, eye, fov_y_, pan, pitch_, pixel_ray, projection (+6 more)

### Community 17 - "Community 17"
Cohesion: 0.19
Nodes (11): dolly, fit, orbit, compile(), optional, Vector3d, link(), init (+3 more)

### Community 18 - "Community 18"
Cohesion: 0.18
Nodes (11): load, SolveJob, error_, result_, start, status_, status_mutex_, status_text (+3 more)

### Community 19 - "Community 19"
Cohesion: 0.25
Nodes (8): cmd_check(), string_view, main(), usage(), Backend, active_backend(), backend_description(), string

### Community 20 - "Community 20"
Cohesion: 0.18
Nodes (11): update_overlays, set, Vector3d, RegionLoad, force, SimSetup, fixtures, loads (+3 more)

### Community 21 - "Community 21"
Cohesion: 0.22
Nodes (5): Vector3d, SizingField, size_at, UniformSizing, h_

### Community 22 - "Community 22"
Cohesion: 0.22
Nodes (9): set_model, string, Model, bbox_max, bbox_min, name, region_count, surface (+1 more)

### Community 23 - "Community 23"
Cohesion: 0.40
Nodes (6): array, DisplayMode, fea_colormap(), bake_result, ensure_framebuffer, render

## Knowledge Gaps
- **172 isolated node(s):** `model`, `setup`, `job`, `result`, `viewport` (+167 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **3 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Viewport` connect `Community 7` to `Community 1`, `Community 2`, `Community 3`, `Community 13`, `Community 14`, `Community 16`, `Community 17`, `Community 20`, `Community 22`, `Community 23`?**
  _High betweenness centrality (0.168) - this node is a cross-community bridge._
- **Why does `NodalMesh` connect `Community 0` to `Community 1`, `Community 8`, `Community 10`, `Community 12`, `Community 13`?**
  _High betweenness centrality (0.122) - this node is a cross-community bridge._
- **Why does `Palette` connect `Community 4` to `Community 14`?**
  _High betweenness centrality (0.104) - this node is a cross-community bridge._
- **Are the 21 inferred relationships involving `src/mesh` (e.g. with `audit` and `ci`) actually correct?**
  _`src/mesh` has 21 INFERRED edges - model-reasoned connections that need verification._
- **What connects `model`, `setup`, `job` to the rest of the system?**
  _172 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Community 0` be split into smaller, more focused modules?**
  _Cohesion score 0.05456095481670929 - nodes in this community are weakly interconnected._
- **Should `Community 1` be split into smaller, more focused modules?**
  _Cohesion score 0.06666666666666667 - nodes in this community are weakly interconnected._