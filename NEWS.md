# Release notes

## 1.3.1 -- FIXME

* Fixed vanilla clouds being shown when "Fancy Graphics" is disabled.
* The scene no longer becomes unplayably dark when underwater or in
  The End.
* Moonlight no longer affects the scene on a rainy night.
* The color of the ambient light is no longer a constant white. It now
  changes depending on the terrain-dependent sunlight level and the
  time-dependent daylight level. That is, when in an occluded area
  like a cave, the only possible light sources are torches so the
  color of ambient light resembles that of torch light. Likewise, when
  on the ground of the Overworld, either the color of the sun or the
  moon will affect the ambient depending on the in-game time.

## 1.3.0 -- 2019-01-06

* Clouds are now slightly brighter at night.
* Introduced a randomness in the brightness of stars.
* Torches now flicker more randomly and slightly more intensely.
* Overhauled the entire lighting passes in the terrain shader. Now it
  computes light levels and colors completely differently. This was
  inevitable to improve lights and fix bugs listed below:

    * The intensity of the ambient light now slightly increases when
      it's foggy (#32).
    * The scene no longer becomes reddish as if it were in the sunset,
      when it rains during the daytime (#24).
    * Dark areas, especially caves, no longer become strangely
      brighter when it rains.
    * Shadows are now much less dense at night.

## 1.2.0 - 2018-12-31

Enhancements:

* Added fake specular light for water and improved its wave. The
  opacity of water surface now changes depending on the angle between
  the camera and the surface. There is still a room for improvement in
  the specular light though. (#10)

Bugfixes:

* Lava pools in the Nether no longer look strangely whitish. (#30)
* Performance improvement for clouds.
* Fixed the color and the intensity of ambient light being calculated
  incorrectly.
* Shadows no longer disappear completely when it rains. It still fades
  suddenly and we're looking for a way to fix it. (#33)
* The animation speed of leaves no longer accelerate when the camera
  is moving. Water still has the same issue but we don't know how to
  fix it. (#36)

## 1.1.0 - 2018-12-26

Enhancements:

* The scene now looks duller under a bad weather condition. (#6)
* Added waves for water and leaves, but not plants due to a limitation
  in the current rendering system. (#10, #11)
* Replaced clouds with non-blocky, shader-generated one.

## 1.0.0 - 2018-12-22

The first release.
