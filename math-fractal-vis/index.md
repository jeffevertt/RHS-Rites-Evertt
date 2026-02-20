# Engineering Challenge: The Fractal Explorer

## The Goal
Create an interactive visualization tool that allows users to explore the infinite complexity of the **Mandelbrot Set** and the **Julia Set**. 

---

## What is a Fractal?
A fractal is a geometric shape that is **self-similar**: no matter how far you zoom in, you find smaller versions of the same patterns. The Mandelbrot set is the most famous example, generated from a simple iterative equation using complex numbers.

## The Math: $z_{n+1} = z_n^2 + c$
To determine if a point on the screen belongs in the set:
1.  Map a pixel $(x, y)$ on your screen to a coordinate on the complex plane, treated as $c = x + yi$.
2.  Start with $z = 0$.
3.  Iterate: Square $z$ and add $c$.
4.  **The Escape Rule:** If the magnitude of $z$ ($|z|$) ever exceeds **2**, the point is "escaping" to infinity and is **not** part of the set. 
5.  **The Iteration Limit:** If the point hasn't escaped after a set number of iterations (e.g., 100 or 1,000), we assume it is "trapped" and color it black.



## How It Works (At a High Level)
* **The Escape-Time Algorithm:** For every pixel on the screen, you run the math loop above. The number of iterations it takes to "escape" determines the color of that pixel.
* **Panning and Zooming:** To zoom, you shrink the range of the complex numbers being mapped to the screen. 
* **The Julia Set:** While the Mandelbrot set keeps $z$ at $0$ and varies $c$, a Julia set keeps $c$ constant and varies the starting $z$. Every point in the Mandelbrot set corresponds to its own unique, beautiful Julia set.

---

## Technical Constraints
1.  **Pure Math:** You may use a library to draw pixels to a window (SDL, SFML, HTML5 Canvas, etc.), but you must implement the complex number arithmetic yourself.
2.  **Interactive Explorer:** The user must be able to pan the view (arrow keys/drag) and zoom in/out (scroll/buttons) in real-time.
3.  **Performance Optimization:** As you zoom deeper, you need more iterations to maintain detail. You must optimize your loops (or use multi-threading) to keep the interaction fluid.
4.  **Color Mapping:** Implement a dynamic color palette. Use the iteration count to create smooth gradients or high-contrast "heat maps."



---

## Technical Milestones
* **Level 1:** Render a static Mandelbrot set in black and white.
* **Level 2:** Implement interactive Pan and Zoom controls.
* **Level 3:** Add "Smooth Coloring" (Renormalization) to remove the distinct bands of color and create silk-like gradients.
* **Level 4:** Implement a "Julia Mode" where the Julia set is rendered based on the mouse's current position within the Mandelbrot set.

## Recommended Resources
* **Complex Number Arithmetic:** Review how to calculate $(x + yi)^2$.
* **The Beauty of Fractals** by Peitgen and Richter (this is a book).
* **Coding Train (YouTube):** "The Mandelbrot Set" and "The Julia Set" tutorials.
* **Smooth Coloring:** Research "Renormalization and the Mandelbrot set" for the log-based coloring formula.

## Example Output
![Fractal Zoom Demo](anim.gif)