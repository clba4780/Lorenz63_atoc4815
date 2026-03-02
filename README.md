This is a multi-file project that produce a figure depicting Lorenze ensemble predictability. This figure should show were the Lorenz attractor has regions where forecasts stay accurate and regions where they immedietly diverge. 

Starting with numerical integration methods using foreward Euler. (integrators.py)
Then apply the numerical integration to the Lorenz 1963 three-variable chaotic model (lorenz63.py)

  The Lorenz (1963) system: a 3-variable model of atmospheric convection.

    Equations
    ---------
    dx/dt = sigma * (y - x)
    dy/dt = rho * x - y - x * z
    dz/dt = x * y - beta * z

    Default parameters (sigma=10, rho=28, beta=8/3) produce chaotic behavior.

Data from vecotrized trajectories is used graph the tendency. (plotting.py)
    
The final experiment is run, starting with a spinup to allow transients to die out. Then a reference trajectory is model using the final     state of the spinup. (run_lorenz_ensemble.py)
