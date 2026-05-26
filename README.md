# ProtoMKR MK2 Protogen Emote Simulator

A browser-based face simulator for HUB75 LED matrix protogen builds.  
Open-source tool by [FallingMapleSJ](https://github.com/FallingMapleSJ).

-----

## What it does

ProtoMKR MK2 lets you design, preview, and tune protogen face animations entirely in your browser — no hardware, no installation, no server required. It simulates two chained 64×32 HUB75 LED panels at full pixel resolution with real animation logic including breathing, blinking, and fluid emote transitions.

- Preview face bitmaps exactly as they will appear on the physical display
- Fine-tune the eye detection zone with live sliders
- Test breathing, blinking, and emote transitions in real time
- Pick eye colors and preview rainbow cycling
- Copy firmware-ready C++ values directly from the tool

-----

## Getting started

1. Download `ProtoMKR_MK2.html`
1. Open it in any modern browser — works as a local file, no server needed
1. The example face loads automatically
1. Tap any expression button to switch faces

**iPad / iPhone:** Save the file to your Files app, then open with any HTML compiler.  
**Desktop:** Double-click or drag into a browser window.

-----

## Uploading expressions

Expressions are **64×32 pixel PNG files** — black background, white pixels for the face.

1. Draw your expression in any pixel art tool (Procreate, Aseprite, Photoshop, etc.)
- Canvas: **64 wide × 32 tall pixels**
- Black background, white face pixels
1. Type a name into the name field in the simulator
1. Tap **ADD** or drop your PNG onto the upload zone
1. Your expression appears as a new button immediately

> The eye should sit in the **right half** of the canvas (roughly x 32–63) and the **top half** (y 0–15) for the eye zone auto-detection to work correctly. The nose and mouth go in the remaining space.

-----

## Eye Zone tool

The eye zone defines which pixels on the canvas are part of the eye. The firmware uses this region for breathing animation and blinking. Getting it right makes the face feel alive.

1. Switch to the expression you want to tune
1. Toggle **SHOW ZONE: ON** — an orange box appears on both panels showing the current eye region
1. Drag the four sliders to tightly wrap the box around your eye pixels:
- **EYE X0** — left edge
- **EYE X1** — right edge
- **EYE Y0** — top edge
- **EYE Y1** — bottom edge
1. The box updates live as you drag
1. When satisfied, tap **COPY C++ VALUES** — the firmware line appears below the button ready to paste into your code

-----

## Color picker

Tap any color swatch to change the eye color across the whole face in real time.  
The **rainbow swatch** (rightmost) starts a continuous hue cycle.

-----

## Animation controls

|Control           |What it does                                            |
|------------------|--------------------------------------------------------|
|**BREATH AMP**    |How far the eye region shifts up and down               |
|**BREATH SPEED**  |Speed of the breathing cycle                            |
|**BLINK SPEED**   |How quickly the eyelid closes and opens                 |
|**BLINK INTERVAL**|Time between automatic blinks                           |
|**MORPH SPEED**   |How fast pixels flow when switching expressions         |
|**AUTO BLINK**    |Toggle automatic blinking on or off                     |
|**EYELID**        |Toggle the eyelid line at the bottom of the blink       |
|**EYE MORPH**     |When ON, the eye region also morphs between expressions |
|**BLINK**         |Trigger a single manual blink                           |
|**MIC VIZ**       |Microphone mouth visualizer (requires serving over HTTP)|

-----

## Tips

- The right panel mirrors automatically — what you see is what the physical display shows
- The orange eye zone box mirrors correctly on both panels
- If your expression has no detectable eye, the zone falls back to sensible defaults — adjust manually with the sliders
- Expression names are matched case-insensitively in firmware
- You can load and preview as many expressions as you like in one session

-----

## License & Copyright

```
Copyright (c) FallingMapleSJ
https://github.com/FallingMapleSJ
All rights reserved.
```

This simulator is open source and available for personal and small-scale commercial use.

**You may:**

- Use this simulator freely for any personal or commercial build
- Share your finished protogen build publicly without crediting this tool
- Modify the code for your own use

**Credit is required when:**

- Redistributing, reposting, or re-uploading this file
- Publishing modified versions of this simulator
- Showcasing the simulator itself — its interface, animation preview, or eye zone tool
- Using this tool as part of a software demonstration, tutorial, or workflow where the simulator, emotion rendering, or export process is what is being shown

**In other words:** the finished costume or build needs no credit. The moment the software (including the rendered emotions), or the rendering pipeline is the only thing display — credit is required. Also if you screenshot progress in the app to share publicly it is preferred that you add credit. (I really think that would help if someone else might want to use this tool.

**You may NOT:**

- Remove or alter the copyright notice at the top of the file
- Claim this tool as your own work

I really hate when I have to add strict rules but yeah. Anyways contact me if you need help or anything at u/FallingMapleSJ or fallingmaplesj@gmail.com

Oh another note: This project was a result of co-development with Sonnet 4.6 by Anthropic. It did take a lot of effort for me though. Revising, editing, tuning and etc was tiring. But the result is good overall.

> Credit: **FallingMapleSJ** — [github.com/FallingMapleSJ](https://github.com/FallingMapleSJ)  
> For licensing questions, open an issue on the GitHub page.

-----

*ProtoMKR MK2 Protogen Emote Simulator — open-source tool by FallingMapleSJ*
