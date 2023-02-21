# skin_functions
How it works https://youtu.be/HsOKwUwL1bE

Set base sprite pixel colours (red,green) to point to coordinates of skin sprite pixel.
Example: base pixel rgb(12,1,9) points to pixel with coordinates of xy(12,1) in skin sprite (blue is ignored).
Shader (sh_apply_skin) then gets color information (rgb values) of that pixel and applies it to base sprite.
Alpha value is used from base sprite.

Skin width and height are same and are power of 2 (1,2,4,8,16,32,...).
Maximum skin dimensions should be 256x256, since rgb values go from 0-255 (256 different values).

Example of use (with provided sprites): draw_sprite_skinned(0,0,sp_test_anim,0,sp_test_skin,0);

Function draw_sprite_skinned draws any sprite with any skin sprite.
Function draw_self_skinned draws objects sprite with skin applied.

Only shader (sh_apply_skin) and script (skin_functions) are needed for it to work.
