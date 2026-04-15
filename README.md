# Audio Reactive Instancing Visuals (TouchDesigner)
Input an audio file and a bunch of cubes responds based on highs and lows of it. 
There is a bunch of geometry instancing and transformations.

## Demo
![Image](https://github.com/user-attachments/assets/bcd97d89-902e-4254-8ca1-67e55dcaea38)

## Architecture
- Audio Device In CHOP → captures live/system audio
- Audio Spectrum / Analyze CHOP → extracts frequency data
- Band separation → low (bass), mid, high frequencies
- Math CHOP → normalization and sensitivity control

## Instancing
- SOP shapes (tube, box, etc.) used as base geometry
- Instancing via CHOP data (position, scale)
- Noise + transform operations for organic motion

Audio drives:

- Instance scale (bass impact)
- Movement / jitter (mids)
- Density / variation (highs)

## Rendering
- Geometry rendered via Render TOP
- Feedback TOP loop for trails and persistence
- Level / Composite / Transform TOPs for visual refinement
- Glow and post-processing effects for enhanced output

