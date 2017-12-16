# otclient-builder
Efficient object builder to modify and create data and sprite objects for the OT Framework.

#To-Do
4 Bytes                ( Dat Signature )
2 Bytes                ( Max Clientid )
2 Bytes                ( Monsters )
2 Bytes                ( Effects )
2 Bytes                ( Distance )

Headers & Subheaders

1 Byte                 ( Header )
--------------------------------------------------------------------------
0x00 - Ground
0x01 - Top Order 1
0x02 - Top Order 2
0x03 - Top Order 3
0x04 - Container
0x05 - Stackable
0x06 - Corpse
0x07 - Useable
0x08 - Rune
0x09 - Writeable       ( 2 Bytes, Text limit )
0x0A - Readable        ( 2 Bytes, Text limit )
0x0B - Fluid
0x0C - Splash
0x0D - Blocking
0x0E - Immoble
0x0F - Blocks Missile
0x10 - Blocks path
0x11 - Pickupable
0x12 - Hangable
0x13 - Horizontal      ( Unsure purpose )
0x14 - Vertical               " "
0x15 - Rotatable
0x16 - Light           ( 2 Bytes Level, 2 Bytes Color )
0x18 - Floorchange
0x19 - Offset          ( 2 Bytes X, 2 Bytes Y Amount of pixels raised)
0x1A - Heighted        ( 2 Bytes, Amount of pixels character raises )
0x1B - Layer           ( Player appears ontop of other sprites to item )
0x1C - Idle Animation
0x1D - Minimap         ( 2 Bytes, Color )
0x1E - Actions         ( 1 Byte, Action #, 1 Byte, usually 4 )
0x1F - Ground item
--------------------------------------------------------------------------

1 Byte                 ( Width )
1 Byte                 ( Length )
1 Byte                 ( Image Cropping, appears if width or height above 1 )
1 Byte                 ( Blendframes )
1 Byte                 ( xdiv )
1 Byte                 ( ydiv )
1 Byte                 ( Unknown )
1 Byte                 ( Animation count )

SpriteCount = (width * height * blendframes * xdiv * ydiv * animcount * unknown)
2 Bytes                ( Spriteid ) * SpriteCount
