# Demo Notes

## Purpose
A standalone creative browser experiment combining SVG marine illustrations, CSS animation, pointer interaction and flocking-inspired fish movement.

## Current implementation
- `index.html` contains the complete scene, styles, illustrations and JavaScript.
- Three decorative whale illustrations float through the scene.
- A fish school responds to pointer movement using simplified separation, cohesion and alignment behavior.
- Bubbles are created and removed dynamically.
- A pointer-following light adds a visual effect.

## Standardization updates
- Removed the unused D3 CDN dependency.
- Removed the hidden system cursor so pointer visibility is preserved.
- Switched pointer tracking to Pointer Events.
- Added support for `prefers-reduced-motion`, including suppression of continuous fish, bubble and whale motion.
- Clarified that the fish behavior is an artistic approximation rather than a scientific simulation.

## Known limitations
- Fish interaction compares every fish with every other fish (quadratic work).
- No build pipeline, automated tests or backend.
- Animation performance varies by device and browser.
- The scene is decorative and has no scientific or operational purpose.

## Future improvements
1. Add pause and motion-intensity controls.
2. Profile and optimize fish-neighborhood calculations.
3. Split styles and scripts into dedicated files if the prototype grows.
4. Add keyboard-accessible controls for future interactions.
