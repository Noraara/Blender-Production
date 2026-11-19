# Verification and recovery

## Match verification to the job

For a small repair, measure or inspect the defect before and after, then check the nearest dependency. For a substantial asset, verify the intended view, evaluated geometry, saved editable source, and any requested export in a clean scene.

Use the relevant QA profile when a specialist is available. Blender can run the core checks directly. Use viewport statistics and evaluated mesh measurements for geometry, the intended camera and a second angle for appearance, and a clean reimport for export checks. Compare against the brief and save the evidence the project permits.

## Scene and mesh checks

- Inspect the intended hero view and a second useful angle. Compare silhouette, proportions, contacts, and shading against the brief. For a reference match, compare from the matched camera. For motion, inspect representative frames and extreme poses.
- Test evaluated geometry. Check dimensions, normals, nonmanifold edges, degenerate geometry, and materials as relevant. Check UVs and texture paths when the asset uses textures. Use a specialist QA profile if available and record checks that were skipped.
- Save a new file or version before destructive work. Keep editable construction in the source. When one asset owns only part of a scene, export from the named objects or an isolated collection.

## Export checks

Reopen the source and reimport the export into a fresh scene as appropriate. Verify the relevant scale, geometry, hierarchy, materials, textures, and pivots. When modifiers change geometry, compare the export to the evaluated source. Use the exporter option that includes evaluated geometry and verify the reimport. Check runtime behavior in the target engine only when it is in scope.

If a live write is interrupted, reconnect and inspect the scene and affected objects before retrying. Report the last verified version, the operation that failed, and where to resume.

## Handoff

Accept or return the `atlas-workflow/v1` packet for mixed work. Include the kind (`context` or `result`), project ID, task ID, and scope. A result should name the changed files, checks actually run, evidence, warnings, and next action. Return to the requesting coordinator. Leave knowledge updates to its knowledge workflow. [Atlas’ Notes packet format](https://github.com/Noraara/Atlas-Notes/blob/main/skills/atlas-notes/assets/packet.md)
