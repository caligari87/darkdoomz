# DarkDoomZ
This simple mutator/add-on re-implements the concept behind SidDoyle's Dark Doom, using ZScript. Basically, makes Doom darker by reducing the light levels across all sectors in the map.

A settings menu is provided to adjust the effect. The following settings are available:

* **Preset** - Eight pre-set lighting levels in 32-unit increments. Equivalents to DarkDoom Lite, Classic, and Black are noted.
* **Mode** - Two adjustment modes are available:
  * **Subtract** - Simply subtracts from the light level. This mimics DarkDoom's method.
  * **Compress** - Applies a linear range commpression, so the light levels don't bottom out as quickly.
  * A third adjustment mode is available by setting `ddz_mode` to `3` in the console. This simply clamps the maximum brightness level without lowering darker sectors. Not exposed in the menu because it doesn't really mesh with the available presets.
* **Fine-Tune** - Adjust the preset darkness setting by +/-16 units.
* **Sky Sectors** - Adjust how much effect is applied to sectors with a sky (full, half, or none)

There is also a flashlight available, with the following settings:

* **Quality**
  * **Simple** - Single spot light using the average spread/intensity of the fancy lights.
  * **Fancy** - Two spot lights to simulate both focused beam and light spill.
* **Type** - Preset light styles. The brighter options may negatively affect performance.
  * **Cheap Incandescent** - Dim warm bulb with a wide beam and little spill.
  * **Midrange Halogen** - Moderately bright, focused beam with large spill.
  * **White LED** - Very bright focused beam, very wide shallow spill
  * **Red Filter** - Dim, nightvision-preserving light, same spread as the halogen.
* **Position** - Where the light is relative to the player and how it moves.
  * **Handheld** - Loose springy following style, from below the viewpoint.
  * **Left / Right Shoulder** - Tighter following, offset to the side of the viewpoint.
  * **Helmet** - Very tight following, above viewpoint
* **Toggle Key** - Customizable hotkey to enable/disable the flashlight.

## Notes

* Presets equivalent to DarkDoom are only intended for subtractive mode. Results will vary with other adjustment modes.
* Sectors modified with ACS or lighting specials may not be properly adjusted. Likewise, mods which rely on checking sector light levels may work differently (or break).
