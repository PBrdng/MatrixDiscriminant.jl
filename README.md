

# MatrixDiscriminant.jl
Computes the discriminant of a matrix by using the determinantal representation from

B. N. Parlett. The (matrix) discriminant as a determinant. Linear Algebra and its Applications 355 (2002) 85-101.

Provides the function `disc()`.

Example:
```julia
using MatrixDiscriminant
A = randn(3,3)
disc(A)
```

For real symmetric matrices there is an option to return a vector, for which the sum of squares of the entries are equal to the discrimant. Example:
Example:

```julia
using MatrixDiscriminant
A = randn(3,3)
S = disc(A+A', SOS = true)
# Now: disc(A+A') = dot(S, S)
```

MatrixDiscriminant.jl also provides support for matrices whose entries are polynomials of type [DynamicPolynomials.jl](https://github.com/JuliaAlgebra/DynamicPolynomials.jl).
