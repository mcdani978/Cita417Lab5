Video Demo: https://www.youtube.com/watch?v=Y8W2NiC9LvQ

Overview

This project demonstrates FPS profiling and optimization in Unreal Engine using a simple test map populated with large numbers of cubes. The goal was to identify performance bottlenecks, apply two optimizations, and show measurable before/after improvements.

Dev Map Summary

The map contains two scenarios:

1. Before Optimization

~20,000 cubes placed densely in one area.

Heavy rendering and CPU overhead.

Measured FPS: ~8.

2. After Optimization

~200 cubes spread throughout the level.

Much lower actor and draw call count.

Measured FPS: 20–30.

Both tests were recorded using the same camera path and setup.

Optimizations Applied
1. Cube Count Reduction

Reducing the number of Static Mesh Actors dramatically lowered draw calls and per-frame processing.
This was the primary source of the FPS improvement.

2. Mobility Review

All cubes were checked for mobility settings (Static / Movable).
This helped identify how mobility settings affect cost, even though the main gain came from reducing actor count.

Before/After Metrics
Scenario	Cube Count	FPS
Before	~20,000	~8
After	~200	20–30
