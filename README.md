# FractalPoint
The FractalPoint (FPI) Number Format 

## About
FractalPoint is a fixed-point number format designed to approximate numbers that typically are part of complex sets, like the Mandelbrot set, in order to perform high precision calculations.

You'll typically run into precision issues when "zooming in" on a mandelbrot render because conventional representations of fractional numbers like the IEEE754 single / double precision can pack only so many bits of precision.

With fixed point representation, that is a "fractional point" declared at an arbitrary position between two bits, you can achieve simpler arithmetic operations because all bits are already aligned.

Fractal point 32-bit (FPI32) is a specific subset of the fixed point representations- there are only 3 integral bits (this is mainly because the mandelbrot fractal, the fractal that I wanted to render, has only a radius of 2. Only 2 integral bits are needed, but I went with 3 just in case), a single sign bit, and the rest 28 a bits for the fraction (close to 10 digits of precision).

```
S = Sign bit
INT = Integral bits
FRACTIONAL = Fractional bits

0 | 000 | 0000 0000 0000 0000 0000 0000 0000 
S   INT   FRACTIONAL BITS

```


This repository will hold implementations from converting to and from FPI32 in various different languages.
