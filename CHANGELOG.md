# Changelog

## 2.1.0 - 2026-07-19

Fork of [Daylily-Zeleen/Godot-DragonBones](https://github.com/Daylily-Zeleen/Godot-DragonBones) v2.0.2, adding runtime animation/skin/bone control and fixing two rendering bugs.

### Added

- **Animation timing** on `DragonBonesArmature` / `DragonBonesArmatureView`:
  - `get_current_animation_time()` / `set_current_animation_time(time)` - read or seek the current animation without stopping it.
  - `get_current_animation_duration()` - length of the current animation.
  - `set_current_animation_loop(enabled)` - toggle looping on the animation that is already playing.
- **Setup-pose resets**:
  - `reset_bones_to_setup_pose(recursively)` - clear accumulated bone animation pose.
  - `reset_slots_to_setup_pose(recursively)` - restore slot display, z-order, color, and deform to setup.
- **Per-slot display swapping** (DragonBones' equivalent of skins):
  - `apply_skin_display(name)` - switch every slot that has it to the matching named display.
  - `get_slot_display_names()` - list each slot's available display names.
- **Persistent bone offsets** that coexist with a playing animation:
  - `set_offset_rotation(radians)` and `set_offset_scale(scale)` on bones.

### Fixed

- Hidden slots (setup `displayIndex < 0`) no longer re-appear every frame, so setup-hidden art/VFX stays hidden.
- Weighted (skinned) meshes no longer break after a slot swaps from an image display back to the mesh.