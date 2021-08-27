# Nonlinear-Diffusion
Solving coupled nonlinear diffusion problem using FTCS method 

@
@t
X(x; t) = DX
@2
@x2X(x; t) + A 􀀀 (B + 1)X(x; t) + X2(x; t)Y (x; t)
@
@t
Y (x; t) = DY
@2
@x2Y (x; t) + B X(x; t) 􀀀 X2(x; t)Y (x; t) :
Interesting solutions are obtained for instance with the following choice of parameters
• Neumann boundary conditions: @X
@x

x=L = 0, @Y
@x

x=L = 0
• Choice of units in which L = 1=2
• DX = 0:001, diffusion constant for substance X
• DY = 0:001, diffusion constant for substance Y
• A = 2 constant concentration of substance A
• B = 5:1 constant concentration of substance B
• h = L=50 spatial discretization length
•  = h2=(10 max[DX;DY ]) temporal discretization length chosen to ensure
the stability of FTCS
• Integrate from t = 0 to t = 10
• Start from the stable solutions perturbed by a random noise
X(x; 0) = A + random noise
Y (x; 0) = B=A + random noise
You can use normally distributed noise, with a standard deviation given by
10% of the central value. (hint: normrnd)
1
Visualize your results using surface or mesh plots. Play with the parameters
DX;DY and B: try to find parameters where the solution converges to the stable
solutions, where it oscillates spatially and where it oscillates both in time and
in space.
