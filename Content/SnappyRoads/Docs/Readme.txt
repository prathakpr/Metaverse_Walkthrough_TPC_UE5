Snappy Roads Blueprint Tool

Lets you quickly and easily snap together a spline based road network.

What's new:

v.2.6 20230207
- Refactor AddSegments functions, more than 60x performance boost!
  - Fix AutoUpdateCollision performance option not working properly
- Use of HISM for MeshExtra to improve performance
- Refactor road segments distribution algorythm
- Refactor, optimize and clean M_MS_RoadLayers material
- Add material M_MS_RoadLayers_v2 which uses  material attribute layers to improve versatility and readability
- Move the main road building logic from the construction script to the event graph to allow the road to be updated automatically from the blueprints
- Refactor and improve Snap! function
- Rewrite and improve ResetOrigin function, now  also affects actor rotation (doesn't support discontinuous splines!)
- Rewrite AttachSplinePoint function for much smaller and readable code
- Full rewrite of Traffic code, reduce code complexity
  - Fix memory leak(every car is spawning a new spline component at each intersection)
  - Relocate BP_SR_Vehicle movement logic to BP_FollowPath_Component
  - New feature: Add 'Preview Path Spline' function to BP_SR_TrafficSpawner
  - New feature: Implement basic collision detection logic
  - New feature: Add rotation offset option for vehicle static mesh
- Organize and clean up UI
- Some minor fixes

v.2.5 20221129
- Organize Assets (Textures, Materials, Meshes)
- New: Add Clean Road Materials
- New Feature: Implement initial support for Material Overrides
- New Feature: Add ability to choose socket ID of an intersection to use as attachment point
- Set pivots of the intersectios meshes to the center of intersecting roads
- Add default socket to the intersections to serve as default attachment point
- Modify GetMeshCapTransform to handle updated intersections
- UI: Overhaul Landscape Deformation category to be less confusing and more consistent with the UE interface
- Landscape: Add support for Layered Mode (EditorApplySpline Node)
- Fix Landscape material not connected Roughness pin
- Rewrite ApplyMeshCapSocketSpline function from scratch making it simpler and more effective
- Rearrange some nodes layouts for better readability

v2.4 20220513
- Add support for World Composition & Sublevels (Soft References)
- Remove dependency of Landscape Blueprint Brush on Landmass plugin
- LinkedRoadsAtEnd/Start buttons now can create linked roads directly without requiring intersection meshes
- Minor UI edits & bug fixes

v2.3 20210323 (unreleased)
- New feature: Support for non-destructive landscape layers(Blueprint Brush)
- New feature: Zscale and other options
- Minor bug fixes

v2.2 20200818
- Various bug fixes
- Add "Add Road Segments Simple" function
- Improve "Fix Wobble" algorithm

v2.1 20200804
- Bug fixes
- New: 2 curb assets

v2.0 20190310
- Add lots of new and improved road and intersection models
- New: Custom collision meshes
- New: Photoscanned 2k road textures
- New feature: Realistic layered road material
  - dynamic or painted road damage/dirt/tar/puddles
  - puddles with depth map
- New feature: Road banking(rotation/roll)
- New feature: Distribute blueprints along roads
- New feature: Snap two roads together without intersection
- Other improvements in snapping algorithm
- Improve vehicle blueprint