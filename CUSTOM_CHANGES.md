# Custom changes (on top of Spatial GUI 1.8, MIT)

1. **Gradient Designer** - Mod Menu -> Spatial GUI opens a hub: *Settings* (YACL) and *Gradient Designer*.
   Up to 8 stops, HSV picker + hex, angle slider, presets, live preview. Stored in `spatial-gui.json5`.
2. **Avatar panel** - the vanilla inventory avatar is removed and a themed panel is drawn on the left:
   animated avatar stage, armour + main/off hand with animated durability bars.
3. **Centered crafting** - 2x2 grid, arrow and result moved to the middle of the inventory, themed.

New code: `theme/`, `ui/`, `client/GradientDesignerScreen`, `client/SpatialGUIHubScreen`,
`mixin/gui/ContainerScreenLayoutMixin`, `mixin/gui/InventoryScreenAvatarMixin`.

## Build
    ./gradlew "Set active project to 26.2-fabric"
    ./gradlew chiseledBuild      # or: ./gradlew :26.2-fabric:build
Needs JDK 25. Requires Fabric API, YACL (not Cloth Config) and optionally Mod Menu.
Only the 26.1.2 / 26.2 Fabric targets are kept; the new code is not written for older versions.
