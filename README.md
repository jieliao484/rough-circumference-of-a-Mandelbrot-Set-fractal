# Rough Circumference of a Mandelbrot Set Fractal

It demonstrates how to approximate the boundary length (circumference) of the Mandelbrot set using bisection search, polynomial fitting, and arc-length integration. The algorithm extracts boundary points of the fractal, fits a polynomial curve to them, and integrates the curve length to provide a rough circumference estimate.

Algorithm:

1. Implement a Mandelbrot divergence test: iterate z_n+1=(z_n)^2+c, classify points as inside or outside depending on whether ∣z∣>2 within 100 iterations.
2. For each real value x in [−2,1], use the bisection algorithm along the imaginary axis to find the boundary point where inside/outside flips.
3. Collect boundary points and mirror them across the real axis for the full outline.
4. Fit a degree-15 polynomial to the boundary points over the interval [−2,0].
5. Compute the arc length using the formula of integration L=sqrt(1+(f'(x))^2)dx within a and b, and double it for both halves to get the total circumference.

How to use:
- Adjust parameters at the top of the script (e.g., number of samples n, polynomial degree, fitting interval [fit1, fit2]).
- The program will plot the raw boundary points, the mirrored lower half, and the fitted polynomial curve.
- The command window will print the estimated upper-half length and total circumference.
