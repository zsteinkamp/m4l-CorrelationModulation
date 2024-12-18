# m4l-CorrelationModulation
## Use left/right phase correlation as a modulation source.

![CorrelationModulation](images/CorrelationModulation.gif)

This is a Max For Live device that uses a stereo signal's left/right phase correlation as a modulation source to control other parameters. It has adjustable smoothing, shift, and scale controls.

A mono signal has a correlation value of 1. A stereo signal that is perfectly out of phase has a correlation value of 0. A , as does a signal at 100% volume in one channel and silence in the other. This device allows you to map that correlation value to up to 8 other parameters in your Live Set.

[Video showing it in action.](https://www.youtube.com/watch?v=YfRTARPEUME)

### Changelog

Direct download links below.
- 2024-10-29 [v3](https://github.com/zsteinkamp/m4l-CorrelationModulation/releases/download/v3/CorrelationModulation-v3.amxd) - Add non-blocking telemetry ping on load. Does not send any identifying information, only the plugin name, the local computer name, type of computer, and CPU type. I just want to see which plugins are used the most.

* 2024-08-17 [v2](https://github.com/zsteinkamp/m4l-CorrelationModulation/raw/main/frozen/CorrelationModulation-v2.amxd) - Support Live 12 Modulation mode; General improvements and UI touch-ups
* 2023-12-09 [v1](https://github.com/zsteinkamp/m4l-CorrelationModulation/raw/main/frozen/CorrelationModulation-v1.amxd) - Initial Version

## Installation / Setup

If you just want to download and install the device, then go to the [frozen/](https://github.com/zsteinkamp/m4l-CorrelationModulation/tree/main/frozen) directory and download the newest `.amxd` file there. You can also download it directly via the links in [*Changelog*](#changelog).

Note: If you want to open and edit the non-frozen device, you will need to have [zs.mapper](https://github.com/zsteinkamp/m4l-zs.mapper) installed. [Follow the installation instructions](https://github.com/zsteinkamp/m4l-zs.mapper) there.

## Usage

Add the device to an instrument or MIDI track. The left/right phase correlation of the incoming stereo audio signal is calculated, smoothed, scaled and shifted. The resulting signal can be used to modulate other parameters in your device chains.

### Smooth
Use the `Smooth` dial to control how many samples are averaged to produce the output value. A higher number will produce smoother output. You can control the smoothing by time or with a note value.

### Curve
Adjusts the power of the curve mapping to the output values. Higher numbers have exaggerated responses to changes in correlation.

### Scale
Scales the output value by the specified value.

### Invert
Inverts the output signal.

### Shift
Increases or decreases the output value by a fixed amount.

## Common Problems

#### ...
...

## TODOs
* ...

