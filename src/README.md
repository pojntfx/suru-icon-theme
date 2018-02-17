## Icon Sources

- Do not edit icon assets directly (i.e. those in the "Suru-Adwaita-Ubuntu" folder)! 
- To modify an icon, edit source SVG files found in this directory (or create a new one using the [Template](Template.svg)) and render them with the appropriate script.
- To edit the icons you will need `inkscape` installed and to use the render scripts you'll need both `python` (to render PNG assets) and `ruby` (to render SVG assets) installed.

## Source Files

The sources for all the different icons are kept organized in this `src` folder for ease of development.

**[fullcolor](./fullcolor)**
 - sources for all full color icons.
 - divided into subfolders that organize the icons sources by `context`

**[source-symbolic.svg](./source-symbolic.svg)**
 - the source plate for all of the symbolic icons
 - layers on the source plate correspond to an icons `context` and the icons are sorted accordingly
 - each icon should be contained within an empty 16x16 pixel square and given a label which is its `icon-name`

## Render Scripts

For simplified development, has various scripts to extract or render icons from the larger SVG source files.

**[extract-symbolic-icons.rb](./extract-symbolic-icons.rb)**
 - This script will extract any new symbolic icons from the [source SVG](./source-symbolic.svg) or extract individual icons when passed the icon name: `./extract-symbolic-icons.rb <icon-name>`. 

**[render-bitmaps.py](./render-bitmaps.py)**
- This script will render PNG icons, provided there are source changes, in both @1x and @2x (HiDPi) resolutions from the source files. 

## Resources

**[Suru-Adwaita-Ubuntu.gpl](./Suru-Adwaita-Ubuntu.gpl)**
- The Inkscape colour palette for the Suru-Adwaita-Ubuntu icons. You can copy it to `.config/inkscape/palettes` and restart Inkscape to able to choose it from the palette menu.

**[Template.svg](./Template.svg)**
 - a blank template file for the fullcolor Suru-Adwaita-Ubuntu icons
 - the template has as _Baseplate_ layer which will contain the necessary metadata for rendering an icon
 - You **must** change the `context` and `icon-name` labels on the _Baseplate_ for an icon to render properly (also hide the layer)