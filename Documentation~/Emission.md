# Emission Settings

Emission controls the color and intensity of light emitted from the surface. When you use an emissive Material in your Scene
, it appears as a visible source of light. The meshes
 appear to be self-illuminated.

<img src="images/EmissiveAnimation.png" height="256">


* [Emission Map](#emission-map)
* [Emission Map Animation](#emission-map-animation)
  * [Base Speed (Time)](#base-speed-time)
  * [Animation Mode](#animation-mode)
  * [Scroll U/X direction](#scroll-ux-direction)
  * [Scroll V/Y direction](#scroll-vy-direction)
  * [Rotate around UV center](#rotate-around-uv-center)
  * [Ping-pong moves for base](#ping-pong-moves-for-base)

  * [Color Shifting with Time](#color-shifting-speed-time)
    * [Destination Color](#destination-color)
    * [Color Shifting Speed (Time)](#color-shifting-speed-time)

  * [Color Shifting with View Angle](#color-shifting-with-view-angle)
    * [Shifting Target Color](#shifting-target-color)


## Emission Map
Primarily used with the Bloom Post Effect, Luminous objects can be represented.
| Emission Map Example |
| -- |
| <img src="images/EmissionMapSample.png" height="256"> | 

## Emission Map Animation
When Enabled, the UV and Color of the Emission Map are animated.

 <img src="images/EmissionAnimation.gif" height="256"> 




### Base Speed (Time)
Specifies the base update speed of scroll animation. If the value is 1, it will be updated in 1 second. Specifying a value of 2 results in twice the speed of a value of 1, so it will be updated in 0.5 seconds.

| Base Speed = 0.5 | Base Speed = 1.5 |
| -- | --|
| <img src="images/EmissionMapBaseSpeedHalf.gif" height="256">| <img src="images/EmissionMapBaseSpeedOneAndHalf.gif" height="256"> |


### Animation Mode
Controls the animated scrolling of the emissive texture.

| UV Coordinate Scroll | View Coordinate Scroll |
| -- | --|
| <img src="images/EmissionMapBaseSpeedHalf.gif" height="256">| <img src="images/EmissionMapViewCoordinateScroll.gif" height="256"> |


### Scroll U/X direction
Specifies how much the Emissive texture should scroll in the u-direction (x-axis direction) when updating the animation. The scrolling animation is ultimately determined by Base Speed (Time) x Scroll U Direction x Scroll V Direction.

### Scroll V/Y direction
Specifies how much the Emissive texture should scroll in the V-direction (y-axis direction) when updating the animation. The scrolling animation is ultimately determined by Base Speed (Time) x Scroll U Direction x Scroll V Direction.

### Rotate around UV center
When Base Speed=1, the Emissive texture will rotate clockwise by 1. When combined with scrolling, rotation will occur after scrolling.

<img src="images/RotateAroundUVCenter3.gif" height="256">

### Ping-pong moves for base
When enabled, you can set PingPong (back and forth) in the direction of the animation.

<img src="images/PingPongMove.gif" height="256">

### Color Shifting with Time
The color that is multiplied by the Emissive texture is changed by linear interpolation (Lerp) toward the Destination Color.

#### Destination Color
Destination color above, must be specified in HDR.

#### Color Shifting Speed (Time)
Sets the reference speed for color shift. When the value is 1, one cycle should take approximately 6 seconds.

<img src="images/ColorShiftingWithTime.gif" height="256">


### Color Shifting with View Angle
Emissive color shifts in accordance with view angle.

#### Shifting Target Color
Target color for Color Shifting with View Angle which must be specified in HDR.

<img src="images/ColorShiftingWithView.gif" height="256">

