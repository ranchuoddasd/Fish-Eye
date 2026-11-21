# Interactive Ocean Animation

A self-contained browser scene exploring SVG illustrations, CSS motion, pointer interaction and a simulated school of fish in a stylized underwater environment.

**Status:** Creative front-end experiment. The scene is decorative and does not represent an ecological or scientific simulation.

## Features

- Original SVG-style whale illustrations.
- CSS-based floating motion and animated bubbles.
- Pointer-responsive fish movement and flocking-inspired behavior.
- Pointer-following ambient light.
- Responsive full-screen scene.
- Reduced-motion preference support.
- No framework, build step or external runtime library required.

## Run

Open `index.html` in a modern browser. The project is a standalone HTML file.

## Project structure

```text
.
├── index.html
├── README.md
└── docs/
    ├── architecture.md
    └── demo-notes.md
```

## Interaction model

The fish respond to pointer position and use simplified separation, cohesion and alignment forces. Their motion is illustrative, not a validated biological schooling model. The scene uses browser animation APIs and CSS keyframes.

## Accessibility and performance

- The page respects the `prefers-reduced-motion` media preference by disabling continuous motion.
- Pointer interaction uses pointer events.
- The fish-neighborhood calculation compares fish pairs and therefore grows quadratically with fish count. Reduce the count or introduce spatial partitioning if extending the scene.
- Decorative motion and pointer effects should not be required to understand page content.

## Limitations

- No backend, data collection or external service integration.
- No automated tests or build pipeline.
- Fish behavior is a visual approximation.
- Performance depends on browser, device and viewport.

## Roadmap

1. Separate CSS and JavaScript into dedicated files if the scene expands.
2. Add a user-controlled pause and motion-intensity setting.
3. Profile animation performance and consider spatial partitioning.
4. Add keyboard-accessible controls for any future interactive features.
5. Add browser-based smoke tests.

## Security

The demo runs locally in the browser and does not require credentials or make application API calls. Keep future external assets and scripts pinned, reviewed and minimal.

## License

No license is currently provided. Until a license is added, reuse and redistribution are not granted by default.
