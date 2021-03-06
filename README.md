# Youtube Emotion Extractor
A tool that builds dataset of emotions for corresponding spoken sentences from Youtube videos using Affectiva API

### Plan
Using Affectiva API, we can detect emotions present in each frame of a Youtube video.

### Limitation and Workaround
Since Affectiva Javascript API is only available in browser, and takes image in form of canvas's `imageData`, this tool will be running in browser instead of in a standalone node.js application. Here's how it works:

1. A Youtube video is loaded into the page, playing under a `video` tag.
2. The playing video is then rendered to play on a `canvas`.
3. Each image frame is pulled from the canvas, and then mapped to words/sentences spoken from Youtube's annotation.

### Resources
These links contain very useful examples:
- https://jsfiddle.net/affectiva/h6p64vwg/show/
- http://html5doctor.com/video-canvas-magic/
