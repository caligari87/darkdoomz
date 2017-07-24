# darkdoomz
This simple mutator/add-on re-implements the concept behind SidDoyle's Dark Doom, using ZScript. Basically, makes Doom darker by reducing the light levels across all sectors in the map.

A settings menu is provided to adjust the effect. The following settings are available:

* **Preset** Eight pre-set lighting levels in 32-unit increments. Equivalents to DarkDoom Lite, Classic, and Black are noted.
* **Mode** Two adjustment modes are available:
 * *Subtract* Simply subtracts from the light level. This mimics DarkDoom's method.
 * *Compress* Applies a linear range commpression, so the light levels don't bottom out as quickly.
 * A third adjustment mode is available by setting `ddz_mode` to `3` in the console. This simply clamps the maximum brightness level without lowering darker sectors. Not exposed in the menu because it doesn't really mesh with the available presets.
* **Fine-Tune** Adjust the preset darkness setting by +/-16 units.

##Notes

* Presets equivalent to DarkDoom are only intended for subtractive mode. Results will vary with other adjustment modes.
* Sectors modified with ACS or lighting specials may not be properly adjusted. Likewise, mods which rely on checking sector light levels may work differently (or break).