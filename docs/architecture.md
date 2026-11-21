# Architecture

## Current browser scene

```text
HTML scene structure
       |
       +--> SVG marine illustrations
       |
       +--> CSS keyframe animation
       |
       +--> FishSchool JavaScript controller
       |       |
       |       +--> Fish initialization
       |       +--> Pointer input
       |       +--> Separation / cohesion / alignment
       |       +--> Position and orientation updates
       |
       +--> Bubble generator
       |
       +--> Whale pointer-parallax effect
```

## Main components

- **Scene markup:** positions the whales, person illustration, fish layer, bubbles and pointer light.
- **SVG illustrations:** define the decorative marine creatures and fish.
- **CSS animations:** animate whales and bubbles.
- **FishSchool:** initializes fish state, listens for pointer movement and updates flocking-inspired motion.
- **Bubble generator:** creates and removes decorative bubbles.
- **Whale interaction:** applies pointer-relative translation to whale elements.

## Motion accessibility

The page checks `prefers-reduced-motion`. When the preference is enabled, continuous JavaScript animation, bubble creation and whale parallax are not started; CSS motion is also minimized.

## Performance considerations

The current fish update loop compares each fish with every other fish to calculate local behavior. This is O(n²) in the number of fish. Spatial hashing or a grid-based neighborhood index would reduce unnecessary comparisons if the population grows.

## Scope

This is an artistic browser animation. It is not a physical fluid model, marine biology simulator or data-driven visualization.
