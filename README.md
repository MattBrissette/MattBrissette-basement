1. Full 3D Studio Environment
This isn’t just rendering a flat page on geometry — it’s a complete photorealistic 3D basement studio, featuring:

Realistic lighting (spotlights, ambient light, wall lighting)
High-quality shadow mapping (2048×2048 shadow maps)
Physically-based materials (roughness, metalness across all objects)

2. Detailed 3D Assets (Procedurally Built)
Every object is hand-coded geometry:

Desk: Four legs, material mat, contact shadows
Monitor: Curved bezel (dynamic geometry), screen stand, chin piece
Speakers: Full woofer + tweeter construction
Keyboard & Mouse: Includes contact shadows
Dust motes: Animated particles floating in 3D space using sine/cosine motion
Lighting rig: Multiple light sources casting realistic shadows

3. Canvas-to-Texture Pipeline
An HTML canvas is rendered directly onto the 3D monitor in real time.

The monitor displays live UI content as a projected texture
Creates a seamless bridge between DOM and 3D environment

4. Smart Camera Behavior
The camera operates in two distinct states:

Normal: Cinematic view (12, 8, 18) with a wide pan range
Zoomed: Close-up on monitor (0, eye level, 7.8) with subtle parallax

Additional behavior:

Uses lerp() for smooth, fluid transitions
Mouse position dynamically controls pan and look-at point based on zoom level

5. Gesture-Based Navigation
Click anywhere (except contact button) → zoom to monitor

Scroll up/down → toggle zoom state
Contextual overlay updates:
“SCROLL TO FOCUS”
“SCROLL TO EXIT”

6. Atmospheric Effects
Film grain overlay (mix-blend-mode: overlay)
Bloom layer with radial gradient (cyan/teal glow)
Animated dust particles with sine-wave motion
Custom cursor with hover-based scale animation

7. Contact Shadow Simulation
Custom createContactShadow() function
Generates soft, realistic shadows beneath objects
Fully dynamic (not baked), with accurate positioning
