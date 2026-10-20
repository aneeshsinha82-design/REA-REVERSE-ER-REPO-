# Motion Lab — Feature Plan

Motion Lab is an original browser-based motion-graphics editor. It is not an Adobe After Effects clone and does not claim feature parity.

## Implemented in the current prototype
- Composition preview with a 16:9 canvas
- Text, rectangle, circle and star layers
- Layer selection, duplication, raising, and deletion
- Transform controls: position, scale, rotation, opacity, dimensions
- Timeline scrubbing and playback
- Transform keyframes with linear, ease-in, ease-out, ease-in-out and hold interpolation
- Basic CSS-based blur, brightness, contrast, saturation, hue rotation, blend modes and text shadow
- JSON project import/export
- SVG still-frame export

## Planned engineering milestones
1. **Core timeline:** duration and frame-rate settings, snapping, clip in/out points, track controls, keyframe editing and a graph editor.
2. **Media pipeline:** import images, video and audio; asset bin; proxies; waveform display; robust project asset management.
3. **Rendering:** frame-accurate preview, WebCodecs/WebAssembly rendering where supported, WebM/MP4 export path, progress/cancel and audio mixing.
4. **Compositing:** masks, track mattes, blend modes, nested compositions, alpha handling and color management.
5. **Effects engine:** modular effect stack, effect parameters and keyframes, GPU acceleration where available, presets and non-destructive ordering.
6. **Motion design:** path animation, shape paths, strokes/fills, text animators, parenting, null objects, motion blur and reusable presets.
7. **3D and camera:** scene graph, lights, camera controls and 3D transforms if a suitable renderer is selected.
8. **Expressions and automation:** a sandboxed expression system, scripting API, reusable templates and batch workflows.
9. **Quality:** automated tests, project versioning/migrations, autosave, undo/redo, accessibility and performance profiling.

## Reverse-engineering workflow
Use REA only on software and data you are authorized to analyze. For each target feature, record reproducible observations and public documentation, create an independent behavioral specification, implement an original equivalent, and test it against that specification. Do not copy Adobe source code, bypass licensing or DRM, or redistribute proprietary assets.

## Current limitations
- No import/playback of video or audio yet
- No rendered video export yet (SVG export is a still frame)
- No masks, 3D scene, expressions, graph editor, motion blur, plugin host, or full effect catalogue
- Keyframes currently animate transform properties only
- Browser CSS effects are a prototype, not a production compositor
