# Graph Report - Polyhedral-FEA  (2026-07-10)

## Corpus Check
- 194 files · ~113,685 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 2023 nodes · 3128 edges · 305 communities (137 shown, 168 thin omitted)
- Extraction: 92% EXTRACTED · 8% INFERRED · 0% AMBIGUOUS · INFERRED: 252 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `dc14e24c`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- VEM & Nodal Mesh
- Grid Classification
- Element Assembly Core
- GUI Viewport GL
- Example Geometries
- Hybrid Graded Fill
- GUI Theme Palette
- Bench Emit Scripts
- SpMV CSR Backend
- CLI Mesh Solve
- Poly Mesh Topology
- GUI App State
- Gmsh MSH Import
- Surface Traction
- Pipeline Scene Jobs
- Structured Mesh Tests
- Surface Projection
- Shape Functions
- Adapt Loop Seeds
- Mixed Cell Fill
- FEA Solve Methods
- Scene Solve Result
- GUI Widgets
- MMS Convergence Tests
- Solve Job Pipeline
- D6 Tier3 Bench
- Viewport Camera
- Sizing Field Blend
- Transition Fill
- CMake Project Build
- Scene Model Bounds
- Geom Indicators
- STL Geometry IO
- TriSurface Geometry
- Sim Setup Loads
- Kirsch Graded Tests
- P-Elevate Elements
- Tet Quality Metrics
- Feature Sizing Field
- GUI Study Panels
- JSON Schema Props
- Tier1 Verification Cases
- Boundary Faces
- Schema Mesh Solve
- Mesh Face Headers
- Competitive Peer Solvers
- Roadmap Phases CUDA
- Geometry Sizing
- Reference Case Bench
- FEA Colormap Display
- Schema Type Props
- Analytical Tier1 Cases
- Geometry Kernel ADR
- Cantilever Iterative
- D6 Scoreboard Bench
- Element Formulations ADR
- CUDA SpMV Kernel
- Feature Graded Error
- Hex Fill Output
- Local Refine Tests
- Audit Bench Policy
- Mesh Spec Layers
- Gate1 Baseline Freeze
- Hybrid Mesher ADR
- HP Mesh Co-Design
- ZZ Stress Recovery
- Geom Features Extract
- L-Domain Solve Tests
- Solve Energy Output
- Root Schema JSON
- Polyhedral Ideas P4P5
- Lame Cylinder Tests
- Backend Bench Smoke
- Resolved Mesh Size
- CUDA Backend ADR
- Adapt Remesh ADR
- ZZ Recovery API
- STEP Geometry Load
- Kirsch Plate Tests
- Theme Apply Palettes
- GL Shader Bind
- Mesh Structure ADR
- GUI Phase ADR
- Mesher Solver Co-Design
- Agent Loop Process
- Quadrature Tests
- Shape Function Tests
- STL IO Tests
- Tet Fill Tests
- GroupBox Frame UI
- Schema DOFs Field
- Schema Version Field
- Schema Wall Time
- Adaptivity Pipeline
- Schema Label Field
- Schema Notes Field
- Schema Solver Field
- Schema Version Meta
- Public Mesh Scripts
- Public Solve Scripts
- Region Pick Optional
- Polymesh Smoke Script
- MMS Convergence Orders
- OpenCASCADE Option
- OpenMP Parallelism
- Tier0 Patch Tests
- BSD-3 License ADR
- polymesh-gui Executable
- Verification
- Context
- ROADMAP — Get PolyMesh off the ground
- unit_box
- bench_harness library
- User-Paintable Region Override (GUI)
- cell_stamp.hpp
- vector
- optional
- string
- VectorXd
- VolumeMesher
- CLAUDE.md — PolyMesh (working name)
- sizing_field.cpp
- ADR-0012: Hybrid meshing — graded tet + true mixed zoo
- ADR-0016: True local h-refine — longest-edge bisection (no hanging nodes)
- ADR-0017: VEM k=2 with serendipity edge midpoints
- SPEC — Adaptive Hybrid Polyhedral Mesher + Co-Designed FEA Solver
- prism_fill_surface
- transition_fill_surface
- BENCHMARKS — Verification Suite & Anti-Cheat Design
- ADR-0010: Mesh data structure — keep face-based; edge index optional
- string
- write_vtu
- ADR-0011: VEM k=1 for polyhedra
- Quickstart (Ubuntu)
- test_d6_bench_smoke.cpp
- apply_theme
- D6 Tier-3 — L-domain uniform tet10 vs graded tet10
- ADR-0001: Geometry kernel — OpenCASCADE for B-rep/STEP, feature-gated; STL always available
- ADR-0002: License — BSD-3-Clause
- ADR-0003: Element formulations — unified trait over isoparametric FEM (p=1..4) + VEM
- ADR-0004: Mesh data structure — face-based owner/neighbour
- ADR-0005: Benchmark baseline — own uniform tet10 path + CalculiX audit cross-check
- ADR-0006: GUI — after the solver core, as phase P6.5
- ADR-0007: Implementation language — C++20
- ADR-0008: CUDA backend for parallelizable kernels
- ADR-0014: A posteriori Dörfler seed remesh
- Idea harvest: fea-madness (Grok-generated spec, 2026-07-10)
- GroupBoxFrame
- case_id
- README.md
- Holdout Geometry Audit Protocol
- CalculiX First Peer Solver Priority
- Code_Aster Third Peer Solver
- Elmer Second Peer Solver
- Competitive Benchmark Harness
- Edge-Case Mesh Fixtures Suite
- Shared-Edge Ray-Parity Grid Fill Fix
- Public Geometry Fixtures Suite
- unit_box.stl Public Fixture
- SimplicialLDLT Direct Sparse Solver
- External Contributor PR Policy
- Double-Only Solver Math
- GUI Presentation-Only Rule
- P1 Solver Baseline Frozen
- Graded tet10 path
- L-domain re-entrant corner case
- Tier-3 targets (≥5× DOF, ≥3× wall time)
- Uniform tet10 baseline path
- CalculiX peer solver
- kirsch-plate case
- PolyMesh solver
- timoshenko-cantilever case
- ZZ Estimator Honesty (Effectivity [0.5, 2])
- Holdout Geometry Anti-Cheat
- Kirsch Plate Circular-Hole Case
- L-Shaped Domain Singularity Case
- Lamé Thick-Walled Cylinder Case
- Tier 0 Correctness Gates
- Tier 1 Analytical Solutions
- Tier 2 Method of Manufactured Solutions
- Timoshenko Cantilever Case
- OpenCASCADE B-rep/STEP
- POLYMESH_WITH_OCC CMake option
- STL path (always compiled)
- ADR-0002 License BSD-3-Clause
- BSD-3-Clause license
- hp-adaptivity (order + size)
- Isoparametric FEM p=1..4
- Virtual Element Method k=1,2
- Wachspress/mean-value polyhedral FEM
- Face-based owner/neighbour mesh
- Half-face/half-edge alternative
- ADR-0005 Benchmark baseline
- CalculiX audit cross-check
- Own uniform tet10 baseline (frozen GATE 1)
- ADR-0006 GUI phase P6.5
- Desktop GUI (GLFW + Dear ImGui + OpenGL)
- Draft voxel mesher v0
- Interwebz v2 GUI theme
- ADR-0007 Language C++20
- C++20 only (CMake + Ninja)
- ADR-0008 CUDA backend
- Batched element stiffness (CUDA target)
- CUDA optional backend
- fea/backend.hpp dispatch layer
- SpMV in CG iterative solves
- ADR-0009 Tier-1 verification setups
- C5 equal-DOF logarithmic grading
- Goodier cavity
- Kirsch plate (SCF=3)
- L-domain Williams singularity
- ADR-0010 Edge vs face mesh store
- Derived edge adjacency index
- Edge-primary topology (rejected)
- ADR-0011 VEM k=1
- ElementType::kPolyVem
- VEM k=1 formulation
- ADR-0012 Hybrid graded tet + mixed zoo
- graded_tet_fill
- Kuhn 6-tet hex split
- mixed_fill / VolumeMesher::kHybrid
- ADR-0013 Hex core + pyramid skin
- expand_hex_core_to_pyramids
- VolumeMesher::kHexPyramid
- Dörfler seed remesh
- ZZ error recovery
- ADR-0015 Cartesian grid-fill limits
- Cartesian grid-fill meshers
- make_bbox_grid (AABB-fitted lattice)
- Ray parity shared-edge dedupe
- Staircasing boundary artifact
- Constrained Delaunay (deferred B1)
- ADR-0016 Local h-refine LEB
- Hanging-node MPCs (deferred)
- mesh::local_refine_tets API
- Rivara longest-edge bisection
- ADR-0017 VEM k=2
- Hex k=2 coincides with hex20 FEM
- VEM k=2 serendipity edge midpoints
- Theme tokens (theme.hpp/cpp)
- Goal-Oriented (Adjoint) Adaptivity
- Seed-Based Voronoi/Laguerre Polyhedral Meshing
- GATE 1 Baseline Freeze
- Phase P0 Decisions & Scaffolding
- Phase P1 Reference Solver Baseline
- Phase P2 Mesh Core + Tet + Validity
- Phase P3 Geometric Feature Hybrid Meshing
- Phase P4 Polyhedral VEM Elements
- Phase P5 Adaptive Loop Product
- Phase P6 Performance Engineering
- Phase P6.5 GUI
- Phase P7 OSS Release Readiness
- Agent loop harness rules
- One iteration = one ROADMAP ID
- ROADMAP/progress/phases source of truth
- CLAUDE.md / agents notes (moved)
- Convergence rate is the metric
- Eigen .inverse() include gotcha
- Hunter-124 commit attribution policy
- src modules geom/mesh/adapt/fea/bench/cli
- No hardcoded benchmark values in solver
- Patch test is sacred
- Mesher-solver co-design
- ADR-0001 OpenCASCADE STEP/B-rep Option
- ADR-0003 Unified Element Interface
- ADR-0004 Face-Based Mesh DS
- ADR-0005 Benchmark Baseline (Uniform Tet10 + CalculiX)
- ADR-0006 GUI In Scope (P6.5)
- ADR-0008 Optional CUDA Backend
- Dörfler Marking
- Geometry-Driven A Priori Sizing
- hp-Adaptive Mesh Co-Design
- Hybrid Element Zoo
- Linear Elastostatics (3D)
- North Star: Heterogeneous hp Mesh + FEA Co-Optimization
- Architecture Pipeline geom→mesh→fea→adapt
- Solution-Driven A Posteriori Adaptivity
- Tier-3 Win Targets (≥5× DOF, ≥3× Wall Time)
- Virtual Element Method (VEM)
- Zienkiewicz–Zhu Superconvergent Patch Recovery
- Cantilever-style boundary conditions
- Cartesian grid product fills (ADR-0015)
- cylinder_prism.stl
- l_domain.stl
- Mesher options (tet|hex|graded|hexpyr|hexvem)
- plate.stl
- polymesh product CLI
- run_mesh_public.sh
- run_solve_public.sh
- unit_box.stl
- VTU output (displacement, von Mises)
- Auto CG Above 8000 Free DOFs
- Element Types: tet/hex/prism/pyramid/VEM polyhedra

## God Nodes (most connected - your core abstractions)
1. `Viewport` - 58 edges
2. `TriSurface` - 57 edges
3. `NodalMesh` - 55 edges
4. `App` - 42 edges
5. `Palette` - 38 edges
6. `FeaError` - 36 edges
7. `Material` - 33 edges
8. `Model` - 25 edges
9. `SolveResult` - 25 edges
10. `SolveJob` - 24 edges

## Surprising Connections (you probably didn't know these)
- `vem_body_load()` --calls--> `body`  [INFERRED]
  src/fea/src/vem.cpp → tests/support/mms.hpp
- `sizing_field` --semantically_similar_to--> `resolve_mesh_size`  [INFERRED] [semantically similar]
  src/adapt/CMakeLists.txt → examples/README.md
- `merge_unique()` --references--> `NodalMesh`  [INFERRED]
  apps/bench/d6_tier3.cpp → src/fea/include/fea/nodal_mesh.hpp
- `make_l_hex_mesh()` --calls--> `add_node()`  [INFERRED]
  tests/test_l_domain.cpp → apps/bench/d6_tier3.cpp
- `promote_tet4_to_tet10()` --calls--> `FeaError`  [INFERRED]
  apps/bench/d6_tier3.cpp → src/fea/include/fea/nodal_mesh.hpp

## Import Cycles
- None detected.

## Communities (305 total, 168 thin omitted)

### Community 0 - "VEM & Nodal Mesh"
Cohesion: 0.07
Nodes (82): BodyForce, Fun, function, kP2Mono, kP2Vec, FeaError, runtime_error, Vector3d (+74 more)

### Community 1 - "Grid Classification"
Cohesion: 0.07
Nodes (42): EdgeKey, GradedTetFillOutput, h_coarse, h_fine, mesh, n_coarse_cells, n_feature_cells, n_fine_cells (+34 more)

### Community 2 - "Element Assembly Core"
Cohesion: 0.10
Nodes (12): Element, num_nodes, order, stiffness, Material, d_matrix, poissons_ratio, youngs_modulus (+4 more)

### Community 3 - "GUI Viewport GL"
Cohesion: 0.05
Nodes (41): DisplayMode, uint32_t, Vector3d, VectorXd, Viewport, background_program_, background_vao_, baked_max_ (+33 more)

### Community 4 - "Example Geometries"
Cohesion: 0.13
Nodes (20): resolve_mesh_size, adapt library, adapt error estimation (error.cpp), adapt loop (loop.cpp), sizing_field, stiffness assembly, CUDA backend (optional), fea library (+12 more)

### Community 5 - "Hybrid Graded Fill"
Cohesion: 0.42
Nodes (8): size_t, span, vector, Vector3d, flat_idx(), stamp_ball(), stamp_feature_cells(), stamp_seed_cells()

### Community 6 - "GUI Theme Palette"
Cohesion: 0.06
Nodes (36): ImVec4, Palette, accent, accent_dim, accent_mid, accent_soft, accent_soft_top, axis_x (+28 more)

### Community 7 - "Bench Emit Scripts"
Cohesion: 0.08
Nodes (34): face_nodes_hex20(), gate1_rows(), hex20_node_count(), main(), Structured hex20 node count for nx×ny×nz cells (8 corners + 12 edge mids)., Nodes on one structured face with n_perp==0 index, na×nb cells on face.      F, Labeled gate1-p1 points for scoreboard (Lamé, Kirsch, cantilever)., ccx_version() (+26 more)

### Community 8 - "SpMV CSR Backend"
Cohesion: 0.09
Nodes (27): Backend, CsrMatrix, col_idx, cols, row_ptr, rows, values, size_t (+19 more)

### Community 9 - "CLI Mesh Solve"
Cohesion: 0.36
Nodes (11): cmd_check(), cmd_mesh(), cmd_solve(), span, string, string_view, VolumeMesher, load_surface() (+3 more)

### Community 10 - "Poly Mesh Topology"
Cohesion: 0.09
Nodes (26): CellId, CellKind, FaceId, Cell, faces, kind, Face, neighbour (+18 more)

### Community 11 - "GUI App State"
Cohesion: 0.07
Nodes (29): App, deform_auto, deform_scale, deform_true_scale, dof_count, hovered_region, job, lmb_drag_px (+21 more)

### Community 12 - "Gmsh MSH Import"
Cohesion: 0.15
Nodes (21): size_t, Vector3d, runtime_error, ValidityError, span, Vector3d, graded_tet_fill_surface(), span (+13 more)

### Community 13 - "Surface Traction"
Cohesion: 0.05
Nodes (57): GmshType, map, string, vector, MshModel, mesh, physical_faces, physical_names (+49 more)

### Community 14 - "Pipeline Scene Jobs"
Cohesion: 0.14
Nodes (24): join_worker, set_status, optional, size_t, span, string, Vector3d, VectorXd (+16 more)

### Community 15 - "Structured Mesh Tests"
Cohesion: 0.14
Nodes (24): Vector3d, NodalMesh, check_validity, elements, nodes, box_hex_mesh(), box_tet_mesh(), cell_corners() (+16 more)

### Community 16 - "Surface Projection"
Cohesion: 0.11
Nodes (20): set, ConformityStats, count, max_distance, mean_distance, size_t, SnapStats, max_residual (+12 more)

### Community 17 - "Shape Functions"
Cohesion: 0.23
Nodes (17): Dynamic, Matrix, VectorXd, ShapeEval, dn, n, ElementType, vector (+9 more)

### Community 18 - "Adapt Loop Seeds"
Cohesion: 0.12
Nodes (21): AdaptSuggestion, h_next, marked_fraction, n_marked, refine_seeds, seed_band, size_t, vector (+13 more)

### Community 19 - "Mixed Cell Fill"
Cohesion: 0.09
Nodes (33): MixedCellKind, array, size_t, uint32_t, uint8_t, vector, Vector3d, MixedCell (+25 more)

### Community 20 - "FEA Solve Methods"
Cohesion: 0.12
Nodes (22): solve_l_mesh(), Dirichlet, dof_values, Index, map, SolveMethod, SolveOptions, cg_max_iters (+14 more)

### Community 21 - "Scene Solve Result"
Cohesion: 0.09
Nodes (23): array, map, uint32_t, vector, VectorXd, SolveResult, boundary_quads, displacement (+15 more)

### Community 22 - "GUI Widgets"
Cohesion: 0.14
Nodes (22): CollectOffendersFn, ClosestPoint, distance, point, triangle, Vector3d, closest_on_surface(), closest_on_surface_brute() (+14 more)

### Community 23 - "MMS Convergence Tests"
Cohesion: 0.27
Nodes (9): VectorXd, energy_norm_error(), ElementType, Expectation, name, order, type, make_mesh() (+1 more)

### Community 24 - "Solve Job Pipeline"
Cohesion: 0.12
Nodes (19): atomic, mutex, load, SolveJob, clear_failure, error_, mesh_only_, result_ (+11 more)

### Community 25 - "D6 Tier3 Bench"
Cohesion: 0.09
Nodes (37): add_node(), array, int64_t, map, string, uint32_t, vector, fill_block_tets() (+29 more)

### Community 26 - "Viewport Camera"
Cohesion: 0.17
Nodes (18): Camera, distance_, dolly, eye, fit, fov_y_, orbit, pan (+10 more)

### Community 27 - "Sizing Field Blend"
Cohesion: 0.24
Nodes (10): vector, GeometrySizing::GeometrySizing(), make_feature_sizing(), make_geometry_sizing(), uint32_t, SharpEdge, dihedral, v0 (+2 more)

### Community 28 - "Transition Fill"
Cohesion: 0.11
Nodes (20): array, size_t, uint32_t, uint8_t, vector, Vector3d, TransitionCell, kind (+12 more)

### Community 29 - "CMake Project Build"
Cohesion: 0.20
Nodes (14): polymesh-d6-tier3 Bench Binary, polymesh CLI Executable, polymesh-gui Executable, POLYMESH_ENABLE_LTO (OFF Default, Eigen-Safe), POLYMESH_NATIVE_ARCH (OFF Default, Eigen-Safe), polymesh CMake Project, POLYMESH_WITH_GUI, src/adapt Library (+6 more)

### Community 30 - "Scene Model Bounds"
Cohesion: 0.17
Nodes (12): set_model, update_overlays, Vector3d, Model, bbox_max, bbox_min, name, region_count (+4 more)

### Community 31 - "Geom Indicators"
Cohesion: 0.19
Nodes (15): vector, VertexCurvature, kappa, VertexThickness, thickness, size_t, uint32_t, Vector3d (+7 more)

### Community 32 - "STL Geometry IO"
Cohesion: 0.14
Nodes (21): GeomError, runtime_error, bounding_diagonal(), path, Soup, load_step(), triangulate_shape(), byte (+13 more)

### Community 33 - "TriSurface Geometry"
Cohesion: 0.12
Nodes (17): map, array, uint32_t, vector, Vector3d, TriSurface, triangles, validate (+9 more)

### Community 34 - "Sim Setup Loads"
Cohesion: 0.14
Nodes (14): VolumeMesher, SimSetup, adapt_leb_waves, adapt_passes, eta_target, fixtures, loads, mesh_size (+6 more)

### Community 35 - "Kirsch Graded Tests"
Cohesion: 0.16
Nodes (15): RadialMap, array, int64_t, Matrix3d, size_t, Vector3d, kirsch_stress(), KirschRun (+7 more)

### Community 36 - "P-Elevate Elements"
Cohesion: 0.14
Nodes (14): ElementTypeCounts, hex20, hex8, other, tet10, tet4, size_t, count_element_types() (+6 more)

### Community 37 - "Tet Quality Metrics"
Cohesion: 0.12
Nodes (26): FaceConformityStats, is_conforming, n_boundary_faces, n_hanging_faces, n_interior_faces, n_nonconforming, n_tet_faces, n_unique_faces (+18 more)

### Community 38 - "Feature Sizing Field"
Cohesion: 0.15
Nodes (11): FeatureSizing, blend_, h_max_, h_min_, size_at, DistanceFn, Vector3d, SizingField (+3 more)

### Community 39 - "GUI Study Panels"
Cohesion: 0.16
Nodes (20): Matrix, uint64_t, Vector3d, array, map, ManufacturedSolution, body, body_force (+12 more)

### Community 40 - "JSON Schema Props"
Cohesion: 0.14
Nodes (14): additionalProperties, properties, required, type, description, type, accuracy, name (+6 more)

### Community 41 - "Tier1 Verification Cases"
Cohesion: 0.22
Nodes (8): ADR-0009: Tier-1 analytical verification setups (Kirsch / Goodier / L-domain), Alternatives, Decision, Gmsh import, Goodier cavity (SCF = 3(9−5ν)/(2(7−5ν))), Kirsch plate (SCF = 3), L-domain (Williams λ ≈ 0.5445), Why

### Community 42 - "Boundary Faces"
Cohesion: 0.27
Nodes (13): add_face(), array, FaceKey, map, uint32_t, vector, emit_element_faces(), extract_boundary_faces() (+5 more)

### Community 43 - "Schema Mesh Solve"
Cohesion: 0.15
Nodes (13): description, minimum, type, mesh, solve, total, description, minimum (+5 more)

### Community 45 - "Competitive Peer Solvers"
Cohesion: 0.05
Nodes (37): Agent procedure (blind), Goals, Holdout geometry audits, Optional peer cross-check (owner), Owner supply (private), Result JSON (metrics only), Roles, Status (+29 more)

### Community 47 - "Geometry Sizing"
Cohesion: 0.17
Nodes (12): GeometrySizing, blend_, curv_frac_, edges_, h_max_, h_min_, kappa_, size_at (+4 more)

### Community 48 - "Reference Case Bench"
Cohesion: 0.07
Nodes (30): Anti-cheat, Assembly change for H2, Constraints (do not break), Context, Critical files, Epic exit (E1), File ownership (to avoid merge thrash), First concrete commits after approval (+22 more)

### Community 49 - "FEA Colormap Display"
Cohesion: 0.23
Nodes (9): element_num_nodes(), ElementType, uint32_t, vector, NodalElement, faces, nodes, type (+1 more)

### Community 50 - "Schema Type Props"
Cohesion: 0.18
Nodes (11): description, type, description, type, properties, host, label, timestamp (+3 more)

### Community 53 - "Cantilever Iterative"
Cohesion: 0.22
Nodes (10): CantileverSetup, bc, length, loads, mesh, nfree, Index, VectorXd (+2 more)

### Community 56 - "CUDA SpMV Kernel"
Cohesion: 0.18
Nodes (11): array, uint32_t, vector, Vector3d, PrismFillOutput, boundary_max_distance, boundary_quads, h (+3 more)

### Community 57 - "Feature Graded Error"
Cohesion: 0.22
Nodes (8): FeatureGradedSizing, alpha_, edges_, h_max_, h_min_, size_at, surface_, vector

### Community 58 - "Hex Fill Output"
Cohesion: 0.20
Nodes (10): HexFillOutput, boundary_max_distance, boundary_quads, h, hexes, nodes, array, uint32_t (+2 more)

### Community 59 - "Local Refine Tests"
Cohesion: 0.40
Nodes (9): array, size_t, uint32_t, vector, Vector3d, extract_tet4(), nearest_tet(), tets_to_nodal() (+1 more)

### Community 60 - "Audit Bench Policy"
Cohesion: 0.67
Nodes (3): Anti-Cheat Boundary (No Hardcoded Refs in src/apps), CI Workflow (build-test + format + grep-audit), CI Grep-Audit Anti-Cheat Job

### Community 61 - "Mesh Spec Layers"
Cohesion: 0.09
Nodes (22): 10. Quick “I am lost” paths, 1. What this repo is, 2. Directory layout (keep it), 3. Where to change what, 4. Engineering standards (non-negotiable), 5. Documentation standards (no slop), 6. How to add a feature (agent checklist), 7. GUI rules (Interwebz) (+14 more)

### Community 62 - "Gate1 Baseline Freeze"
Cohesion: 0.40
Nodes (4): 1. PLAN, 2. BUILD, 3. VERIFY, 4. LOOP OR STOP

### Community 63 - "Hybrid Mesher ADR"
Cohesion: 0.22
Nodes (8): ADR-0013: Hex core + pyramid skin transition mesher, Decision, Jacobian safety (B3), Nonconformity (why native hex8 + pyramid5 fails the patch test), Orientation, Product FE path (C1 honesty), Surface snap, Why

### Community 64 - "HP Mesh Co-Design"
Cohesion: 0.15
Nodes (12): ASCII convergence (log₂ energy error vs refinement step), GATE 1 — P1 baseline convergence report, Goodier SCF bar, Infrastructure landed with GATE 1, Kirsch SCF bar, L-domain energy self-convergence, Open items deferred past GATE 1, Owner action (+4 more)

### Community 65 - "ZZ Stress Recovery"
Cohesion: 0.33
Nodes (8): Dynamic, Matrix, Stress, Vector3d, VectorXd, element_centroid(), recover_zz(), stress_at()

### Community 66 - "Geom Features Extract"
Cohesion: 0.36
Nodes (8): size_t, span, vector, Vector3d, detect_sharp_edges(), distance_to_features(), point_segment_distance(), tri_normal()

### Community 67 - "L-Domain Solve Tests"
Cohesion: 0.18
Nodes (10): uint32_t, VectorXd, LSolve, energy, mesh, peak_vm_at_corner, u, make_l_hex_mesh() (+2 more)

### Community 68 - "Solve Energy Output"
Cohesion: 0.22
Nodes (11): array, DisplayMode, uint32_t, vector, fea_colormap(), bake_result, ensure_framebuffer, render (+3 more)

### Community 69 - "Root Schema JSON"
Cohesion: 0.25
Nodes (7): additionalProperties, description, $id, required, $schema, title, type

### Community 71 - "Lame Cylinder Tests"
Cohesion: 0.22
Nodes (7): cantilever_setup(), path, write_box_stl(), box_end_regions(), path, write_box_stl(), thread

### Community 72 - "Backend Bench Smoke"
Cohesion: 0.22
Nodes (7): graphify, Polyhedral-FEA — agent notes, Benchmark table, Current phase, Done, Open issues, PROGRESS

### Community 73 - "Resolved Mesh Size"
Cohesion: 0.52
Nodes (6): b_matrix(), Dynamic, Matrix, MatrixXd, element_coords(), element_stiffness()

### Community 76 - "ZZ Recovery API"
Cohesion: 0.14
Nodes (10): Stress, vector, ZzRecovery, element_eta, global_eta, nodal_stress, array, int64_t (+2 more)

### Community 77 - "STEP Geometry Load"
Cohesion: 0.23
Nodes (19): CartesianGrid, cell, nx, ny, nz, origin, cells_for_extent(), classify_cells_inside() (+11 more)

### Community 78 - "Kirsch Plate Tests"
Cohesion: 0.25
Nodes (7): size_t, LocalRefineStats, n_bisections, n_input_tets, n_marked, n_new_nodes, n_output_tets

### Community 79 - "Theme Apply Palettes"
Cohesion: 0.33
Nodes (5): ADR-0018: Graded tet conformity via LEB (not 2:1 hanging Kuhn), Alternatives rejected, Consequences, Context, Decision

### Community 80 - "GL Shader Bind"
Cohesion: 0.47
Nodes (6): bind_line_attr(), compile(), link(), init, GLenum, GLuint

### Community 82 - "GUI Phase ADR"
Cohesion: 0.50
Nodes (3): Adding a colorscheme, GUI theme & layout, Rules

### Community 84 - "Agent Loop Process"
Cohesion: 0.22
Nodes (8): Agent loop — harness rules for finishing PolyMesh, GUI verification (DISPLAY may be missing), `/loop` vs this file, One iteration = one ROADMAP ID (or one vertical story), Parallelism, Session start checklist, Source of truth, Stuck protocol

### Community 85 - "Quadrature Tests"
Cohesion: 0.27
Nodes (18): begin_field(), button(), checkbox(), ImVec4, draw_accent_fill(), draw_box(), draw_centered_label(), end_group_box() (+10 more)

### Community 86 - "Shape Function Tests"
Cohesion: 0.40
Nodes (4): ElementType, vector, Vector3d, interior_points()

### Community 87 - "STL IO Tests"
Cohesion: 0.50
Nodes (4): as_bytes(), byte, string_view, vector

### Community 88 - "Tet Fill Tests"
Cohesion: 0.40
Nodes (4): Case, path, volume, unit_box()

### Community 89 - "GroupBox Frame UI"
Cohesion: 0.40
Nodes (5): Stress, vector, VectorXd, recover_nodal_stress(), von_mises()

### Community 90 - "Schema DOFs Field"
Cohesion: 0.50
Nodes (4): description, minimum, type, dofs

### Community 91 - "Schema Version Field"
Cohesion: 0.50
Nodes (4): schema_version, const, description, type

### Community 92 - "Schema Wall Time"
Cohesion: 0.50
Nodes (4): wall_time_s, additionalProperties, required, type

### Community 94 - "Schema Label Field"
Cohesion: 0.20
Nodes (14): size_t, string, draw_colorbar(), draw_frame(), draw_study_panel(), draw_viewport_content(), drop_callback(), is_geometry_path() (+6 more)

### Community 95 - "Schema Notes Field"
Cohesion: 0.67
Nodes (3): description, type, notes

### Community 96 - "Schema Solver Field"
Cohesion: 0.67
Nodes (3): solver, description, type

### Community 97 - "Schema Version Meta"
Cohesion: 0.67
Nodes (3): version, description, type

### Community 100 - "Region Pick Optional"
Cohesion: 0.25
Nodes (8): size_t, string, ResolvedMeshSize, auto_chosen, h, min_feature_length, n_sharp_edges, note

### Community 119 - "Verification"
Cohesion: 0.14
Nodes (10): P0 — Decisions & scaffolding, P1 — Reference solver on standard elements (the trustworthy baseline), P2 — Mesh core + tet meshing + validity, P3 — Geometric feature analysis → a priori hybrid meshing, P4 — Polyhedral elements (VEM) [parallel with P3 after P2], P5 — Adaptive loop (the product), P6.5 — GUI (ADR-0006), P6 — Performance engineering (+2 more)

### Community 121 - "ROADMAP — Get PolyMesh off the ground"
Cohesion: 0.15
Nodes (13): Agent loop protocol (how to finish this), Current status snapshot, Parallel tracks, Recommended order (critical path to “usable product”), ROADMAP — Get PolyMesh off the ground, Track A — GUI (P6.5 pulled forward), Track B — Mesh quality (P2 remaining), Track C — Hybrid / features (P3 + P4) (+5 more)

### Community 122 - "unit_box"
Cohesion: 0.17
Nodes (12): Benchmark scoreboard, Building (options), CUDA backends (`POLYMESH_WITH_CUDA`), Layout (short), License, Linear solve (direct / CG), Mesh path caveat, OpenMP assembly (`POLYMESH_WITH_OPENMP`) (+4 more)

### Community 125 - "cell_stamp.hpp"
Cohesion: 0.24
Nodes (10): BenchError, runtime_error, ReferenceCase, citation, name, values, path, string (+2 more)

### Community 126 - "vector"
Cohesion: 0.18
Nodes (9): Public geometry fixtures, Usage, Manual one-liners, Mesh only (auto h0), Notes, PolyMesh examples, Prerequisites, Scripts (+1 more)

### Community 127 - "optional"
Cohesion: 0.20
Nodes (10): Agent system prompt (paste this), CHANGES.md — Agent instructions for external PRs, Correct clone (do this first — most failures start here), Hard rules, Merge responsibility, Mission, Open the PR, Start work (every session) (+2 more)

### Community 128 - "string"
Cohesion: 0.20
Nodes (10): ADR-0015: Cartesian grid-fill limits (not Delaunay / frontal), Consequences, Context, Decision, Follow-on, Lattice construction (bbox-fitted), Ray parity (shared-edge dedupe), Staircasing and when they fail (+2 more)

### Community 129 - "VectorXd"
Cohesion: 0.27
Nodes (9): __global__, csr_spmv_kernel(), size_t, string, T, cuda_free(), device_available(), device_name() (+1 more)

### Community 130 - "VolumeMesher"
Cohesion: 0.22
Nodes (10): string, vector, VectorXd, VtuCellData, name, scalars, VtuPointData, name (+2 more)

### Community 131 - "CLAUDE.md — PolyMesh (working name)"
Cohesion: 0.22
Nodes (8): CLAUDE.md — PolyMesh (working name), Definitions of done, Git & attribution, Language & tooling, Licensing, Moved, Non-negotiable engineering rules, Workflow

### Community 132 - "sizing_field.cpp"
Cohesion: 0.31
Nodes (8): dist_, blend_to_max(), clamp_size(), DistanceFn, Vector3d, FeatureSizing::FeatureSizing(), FeatureSizing::size_at(), GeometrySizing::size_at()

### Community 133 - "ADR-0012: Hybrid meshing — graded tet + true mixed zoo"
Cohesion: 0.25
Nodes (7): ADR-0012: Hybrid meshing — graded tet + true mixed zoo, Alternatives rejected for now, Context, Decision (v1 — graded all-tet), Decision (v2 — SPEC hybrid zoo), Deferred, Related mono paths

### Community 134 - "ADR-0016: True local h-refine — longest-edge bisection (no hanging nodes)"
Cohesion: 0.25
Nodes (7): ADR-0016: True local h-refine — longest-edge bisection (no hanging nodes), Alternatives considered, API, Context, Decision, Guarantees / limits, Related

### Community 135 - "ADR-0017: VEM k=2 with serendipity edge midpoints"
Cohesion: 0.25
Nodes (7): Acceptance (ROADMAP C4), ADR-0017: VEM k=2 with serendipity edge midpoints, Alternatives considered, API, Decision, General polyhedra (incremental), Hex serendipity path (ROADMAP C4 acceptance)

### Community 136 - "SPEC — Adaptive Hybrid Polyhedral Mesher + Co-Designed FEA Solver"
Cohesion: 0.25
Nodes (7): Architecture (pinned), Decisions — ratified at GATE 0 (2026-07-09; full rationale in docs/decisions/), Goals, Key technical positions (pinned unless a phase proves otherwise), Non-goals (v1), Problem statement, SPEC — Adaptive Hybrid Polyhedral Mesher + Co-Designed FEA Solver

### Community 137 - "prism_fill_surface"
Cohesion: 0.61
Nodes (7): check_prism_fill_geometry(), Vector3d, pick_sweep_axis(), prism_fill_surface(), prism_signed_volume(), prism_signed_volume_impl(), tet_signed_volume_impl()

### Community 138 - "transition_fill_surface"
Cohesion: 0.46
Nodes (7): cell_inverted(), array, vector, Vector3d, hex8_jacobian_det(), tet_signed_vol(), transition_fill_surface()

### Community 139 - "BENCHMARKS — Verification Suite & Anti-Cheat Design"
Cohesion: 0.29
Nodes (6): Anti-cheat / adversarial audit design, BENCHMARKS — Verification Suite & Anti-Cheat Design, Tier 0 — Correctness gates (must pass exactly, every commit), Tier 1 — Analytical solutions (energy-norm + peak-stress error targets), Tier 2 — Method of Manufactured Solutions (MMS), Tier 3 — Performance benchmarks (the "win" metric)

### Community 140 - "ADR-0010: Mesh data structure — keep face-based; edge index optional"
Cohesion: 0.29
Nodes (6): ADR-0010: Mesh data structure — keep face-based; edge index optional, Alternatives, Context, Decision, Rejected for now, Why face-based wins for PolyMesh

### Community 141 - "string"
Cohesion: 0.29
Nodes (3): string, path, unique_temp_vtu()

### Community 142 - "write_vtu"
Cohesion: 0.38
Nodes (6): ElementType, path, vector, tet4_cell_quality(), vtk_cell_type(), write_vtu()

### Community 143 - "ADR-0011: VEM k=1 for polyhedra"
Cohesion: 0.33
Nodes (5): ADR-0011: VEM k=1 for polyhedra, Alternatives, Decision, Formulation, Why

### Community 144 - "Quickstart (Ubuntu)"
Cohesion: 0.33
Nodes (6): CLI examples (public unit box), Clone, configure, build, test, Dependencies, GUI, Performance build notes, Quickstart (Ubuntu)

### Community 145 - "test_d6_bench_smoke.cpp"
Cohesion: 0.47
Nodes (4): string, run_cmd(), slurp(), temp_out_path()

### Community 146 - "apply_theme"
Cohesion: 0.60
Nodes (4): apply_theme(), make_interwebz_palette(), make_slate_palette(), ThemeId

### Community 147 - "D6 Tier-3 — L-domain uniform tet10 vs graded tet10"
Cohesion: 0.40
Nodes (4): D6 Tier-3 — L-domain uniform tet10 vs graded tet10, Headline (equal strain-energy match, 0.01% tol), Ratios (uniform / graded), Reproduce

### Community 148 - "ADR-0001: Geometry kernel — OpenCASCADE for B-rep/STEP, feature-gated; STL always available"
Cohesion: 0.40
Nodes (4): ADR-0001: Geometry kernel — OpenCASCADE for B-rep/STEP, feature-gated; STL always available, Alternatives, Decision, Why

### Community 149 - "ADR-0002: License — BSD-3-Clause"
Cohesion: 0.40
Nodes (4): ADR-0002: License — BSD-3-Clause, Alternatives considered, Decision, Why

### Community 150 - "ADR-0003: Element formulations — unified trait over isoparametric FEM (p=1..4) + VEM"
Cohesion: 0.40
Nodes (4): ADR-0003: Element formulations — unified trait over isoparametric FEM (p=1..4) + VEM, Alternatives, Decision, Why

### Community 151 - "ADR-0004: Mesh data structure — face-based owner/neighbour"
Cohesion: 0.40
Nodes (4): ADR-0004: Mesh data structure — face-based owner/neighbour, Alternatives, Decision, Why

### Community 152 - "ADR-0005: Benchmark baseline — own uniform tet10 path + CalculiX audit cross-check"
Cohesion: 0.40
Nodes (4): ADR-0005: Benchmark baseline — own uniform tet10 path + CalculiX audit cross-check, Alternatives, Decision, Why

### Community 153 - "ADR-0006: GUI — after the solver core, as phase P6.5"
Cohesion: 0.40
Nodes (4): ADR-0006: GUI — after the solver core, as phase P6.5, Alternatives, Decision, Why

### Community 154 - "ADR-0007: Implementation language — C++20"
Cohesion: 0.40
Nodes (4): ADR-0007: Implementation language — C++20, Alternatives, Decision, Why

### Community 155 - "ADR-0008: CUDA backend for parallelizable kernels"
Cohesion: 0.40
Nodes (4): ADR-0008: CUDA backend for parallelizable kernels, Alternatives, Constraints acknowledged, Decision

### Community 156 - "ADR-0014: A posteriori Dörfler seed remesh"
Cohesion: 0.40
Nodes (4): ADR-0014: A posteriori Dörfler seed remesh, CLI / GUI, Decision, Why

### Community 157 - "Idea harvest: fea-madness (Grok-generated spec, 2026-07-10)"
Cohesion: 0.40
Nodes (4): Assessment, Idea harvest: fea-madness (Grok-generated spec, 2026-07-10), Rejected / deferred, Worth incorporating

### Community 158 - "GroupBoxFrame"
Cohesion: 0.50
Nodes (4): GroupBoxFrame, start, title, width

### Community 159 - "case_id"
Cohesion: 0.67
Nodes (3): description, type, case_id

## Ambiguous Edges - Review These
- `adapt loop (loop.cpp)` → `FEA solve`  [AMBIGUOUS]
  src/adapt/CMakeLists.txt · relation: conceptually_related_to

## Knowledge Gaps
- **845 isolated node(s):** `energy`, `free_dofs`, `nnodes`, `nelems`, `mesh_s` (+840 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **168 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `adapt loop (loop.cpp)` and `FEA solve`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **Why does `Viewport` connect `GUI Viewport GL` to `Solve Energy Output`, `Poly Mesh Topology`, `GUI App State`, `Mesh Face Headers`, `GL Shader Bind`, `Context`, `Viewport Camera`, `Scene Model Bounds`?**
  _High betweenness centrality (0.074) - this node is a cross-community bridge._
- **Why does `NodalMesh` connect `Structured Mesh Tests` to `VEM & Nodal Mesh`, `GroupBox Frame UI`, `ZZ Stress Recovery`, `L-Domain Solve Tests`, `P-Elevate Elements`, `Resolved Mesh Size`, `Boundary Faces`, `Surface Traction`, `write_vtu`, `FEA Colormap Display`, `FEA Solve Methods`, `Scene Solve Result`, `Cantilever Iterative`, `MMS Convergence Tests`, `D6 Tier3 Bench`, `Local Refine Tests`?**
  _High betweenness centrality (0.053) - this node is a cross-community bridge._
- **Why does `TriSurface` connect `TriSurface Geometry` to `STL Geometry IO`, `Geom Features Extract`, `Hybrid Graded Fill`, `CLI Mesh Solve`, `prism_fill_surface`, `transition_fill_surface`, `Gmsh MSH Import`, `string`, `STEP Geometry Load`, `Geometry Sizing`, `Surface Projection`, `Pipeline Scene Jobs`, `GUI Widgets`, `Tet Fill Tests`, `Feature Graded Error`, `Sizing Field Blend`, `Scene Model Bounds`, `Geom Indicators`?**
  _High betweenness centrality (0.050) - this node is a cross-community bridge._
- **What connects `energy`, `free_dofs`, `nnodes` to the rest of the system?**
  _874 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `VEM & Nodal Mesh` be split into smaller, more focused modules?**
  _Cohesion score 0.07053291536050156 - nodes in this community are weakly interconnected._
- **Should `Grid Classification` be split into smaller, more focused modules?**
  _Cohesion score 0.07400555041628122 - nodes in this community are weakly interconnected._