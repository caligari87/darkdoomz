# DarkDoomZ
This simple mutator/add-on re-implements the concept behind SidDoyle's Dark Doom, using ZScript. Basically, makes Doom darker by reducing the light levels across all sectors in the map.

A settings menu is provided to adjust the effect. The following settings are available:

## Main Settings
* **Mode** - Several adjustment modes are available:
  * **Subtract** - Simply subtracts from the light level. This mimics DarkDoom's method.
  * **Compress** - Applies a linear range commpression, so the light levels don't bottom out as quickly.
  * **Clamp** - Clamps the maximum brightness level without lowering darker sectors.
  * **Crush** - Darkens darker sectors more on an exponential curve, adding contrast.
  * **DarkDoom** - Three additional modes to emulate classic DarkDoom. These override the preset darkening settings.
* **Preset** - Eight pre-set lighting levels in 32-unit increments.

## Advanced Settings
* **Pre-Gain** - Adjust the level brightness *before* applying adjustments.
* **Post-Gain** - Adjust the level brightness *after* applying adjustments.
* **Min. Lightlevel** - Enforces a minimum light level regardless of other settings.
* **Sky Sectors** - Adjust how much effect is applied to sectors with a sky.
  * `0.0` = No effect (sky sectors are not adjusted)
  * `0.5` = Half (sky sectors get half adjustment of other sectors)
  * `1.0` = Full effect (sky sectors are adjusted like all other sectors)
* **Sector Effects** - Enables or disables sector light effects (flicker, pulse, etc). Requires a restart of the map.

## Fog Settings
* **Fog Mode** - Alias to GZDoom's built-in light fade setting.
* **Fog Density** - Overrides the default light fade intensity. Can make maps really dark at a distance even in brighter areas.

## Flashlight Settings
* **Quality**
  * **Simple** - Single spot light using the average spread/intensity of the fancy lights.
  * **Fancy** - Two spot lights to simulate both focused beam and light spill.
* **Type** - Preset light styles. The brighter options may negatively affect performance.
  * **Incandescent** - Dim warm bulb with a wide beam and little spill.
  * **Halogen** - Moderately bright, focused beam with large spill.
  * **LED** - Very bright focused beam, very wide shallow spill
  * **Red Filter** - Dim, nightvision-preserving light, same spread as the halogen.
* **Position** - Where the light is relative to the player and how it moves.
  * **Handheld** - Loose springy following style, from below the viewpoint.
  * **Left / Right Shoulder** - Tighter following, offset to the side of the viewpoint.
  * **Helmet** - Very tight following, above viewpoint
* **Toggle Key** - Customizable hotkey to enable/disable the flashlight.
