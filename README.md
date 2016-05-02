# MLPlots

[![Build Status](https://travis-ci.org/JuliaML/MLPlots.jl.svg?branch=master)](https://travis-ci.org/JuliaML/MLPlots.jl)

WIP: Common plotting recipes for statistics and machine learning.

This package uses [Plots.jl](https://github.com/tbreloff/Plots.jl) to provide high-level statistical and machine learning plotting
recipes which are independent of both the platform and graphical library.

Correlation grids:

```julia
using MLPlots
M = randn(1000, 4)
M[:,2] += 0.8M[:,1]
M[:,3] -= 0.7M[:,1]
corrplot(M, size=(700,700))
```

![corrplot_example](docs/corrplot_example.png)


Neural nets with OnlineAI:

```julia
using OnlineAI, MLPlots
net = buildClassificationNet(3, 1, [15,10,5])
plot(net)
```

![onlineai](test/refimg/onlineai1.png)



See the issues for a TODO list.  Collaboration is very welcome.
