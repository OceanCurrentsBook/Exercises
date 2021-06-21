The equations for inertial oscillations are du/dt=fv and dv/dt=-fu

a. Under which conditions does this balance follow from the momentum equations?

b. In python or Matlab, write a code that computes and draws this oscillation. 
For this, first realise that du/dt can be written as du/dt=(u_(n+1)-u_n)/Δt. 
Then iteratively solve the set of equations for 1000 steps with dt=100 s and f=10^(-4) s-1.

c. Why does the circle not exactly close? How does that change if you decrease dt to 10 s (and simultaneously increase the number of time steps to 10,000)?
