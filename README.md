# LHCb data analysis experiments

This is a repository for demonstrating that cool new data analysis method you came up with,
or to show how we might use that new library you found.

# Contents

## Likelihood fits with automatic differentiation

Author: Igor Babuschkin

[Automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) (AD)
allows you to calculate the derivatives of a function more precisely, and
possibly faster than the commonly used finite differences method.  This is
achieved by exploiting the exact structure of the code that implements the
function.

*Reverse mode* AD is particularly useful if you need to calculate the
derivatives of a scalar-valued function with many inputs, as is the case for
the log-likelihood function of a statistical model.

The [autograd](https://github.com/HIPS/autograd) package implements reverse
mode AD for the Python programming language, and makes it particularly easy to
experiment with AD, as it is a drop-in package that seamlessly integrates with
idiomatic Python code using the numpy and scipy packages.

In this notebook, I demonstrate how autograd can be used to provide the
gradient of a simple model consisting of a mixture of two normal distributions,
and minimize the log-likelihood for a randomly generated dataset using this
gradient.

In addition, I demonstrate how to apply transformations on some of the
parameters to remove physical boundaries from the minimization process.

[Link to Jupyter notebook](/Likelihood with autodiff.ipynb)

