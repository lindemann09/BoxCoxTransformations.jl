# BoxCoxTransformations

[![Build Status](https://github.com/lindemann09/BoxCoxTransformations.jl/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/lindemann09/BoxCoxTransformations.jl/actions/workflows/CI.yml?query=branch%3Amain)


Wraps currently [BoxCoxTrans.jl](https://github.com/tk3369/BoxCoxTrans.jl)
and provides confidence intervals ([see doc](https://lindemann09.github.io/BoxCoxTransformations.jl/)).

```
using BoxCoxTransformations
using Distributions

x = rand(Gamma(2,2), 10000) .+ 1;

bc = fit(BoxCoxTransformation, x)

# lambda parameter
bc.lambda

# confidence intervall for lambda
confint(bc)

# transformed data
transform(bc)
```

See [BoxCoxTransformationsMakie.jl](https://github.com/lindemann09/BoxCoxTransformationsMakie.jl) for BoxCox-plots.