# qiskit.algorithms.optimizers.POWELL

<span id="undefined" />

`POWELL(maxiter=None, maxfev=1000, disp=False, xtol=0.0001, tol=None, options=None, **kwargs)`

Powell optimizer.

The Powell algorithm performs unconstrained optimization; it ignores bounds or constraints. Powell is a *conjugate direction method*: it performs sequential one-dimensional minimization along each directional vector, which is updated at each iteration of the main minimization loop. The function being minimized need not be differentiable, and no derivatives are taken.

Uses scipy.optimize.minimize Powell. For further detail, please refer to See [https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.minimize.html](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.minimize.html)

**Parameters**

*   **maxiter** (`Optional`\[`int`]) – Maximum allowed number of iterations. If both maxiter and maxfev are set, minimization will stop at the first reached.
*   **maxfev** (`int`) – Maximum allowed number of function evaluations. If both maxiter and maxfev are set, minimization will stop at the first reached.
*   **disp** (`bool`) – Set to True to print convergence messages.
*   **xtol** (`float`) – Relative error in solution xopt acceptable for convergence.
*   **tol** (`Optional`\[`float`]) – Tolerance for termination.
*   **options** (`Optional`\[`dict`]) – A dictionary of solver options.
*   **kwargs** – additional kwargs for scipy.optimize.minimize.

<span id="undefined" />

`__init__(maxiter=None, maxfev=1000, disp=False, xtol=0.0001, tol=None, options=None, **kwargs)`

**Parameters**

*   **maxiter** (`Optional`\[`int`]) – Maximum allowed number of iterations. If both maxiter and maxfev are set, minimization will stop at the first reached.
*   **maxfev** (`int`) – Maximum allowed number of function evaluations. If both maxiter and maxfev are set, minimization will stop at the first reached.
*   **disp** (`bool`) – Set to True to print convergence messages.
*   **xtol** (`float`) – Relative error in solution xopt acceptable for convergence.
*   **tol** (`Optional`\[`float`]) – Tolerance for termination.
*   **options** (`Optional`\[`dict`]) – A dictionary of solver options.
*   **kwargs** – additional kwargs for scipy.optimize.minimize.

## Methods

|                                                                                                                                                                    |                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- |
| [`__init__`](#qiskit.algorithms.optimizers.POWELL.__init__ "qiskit.algorithms.optimizers.POWELL.__init__")(\[maxiter, maxfev, disp, xtol, tol, …])                 | **type maxiter**`Optional`\[`int`]                                                                        |
| [`get_support_level`](#qiskit.algorithms.optimizers.POWELL.get_support_level "qiskit.algorithms.optimizers.POWELL.get_support_level")()                            | Return support level dictionary                                                                           |
| [`gradient_num_diff`](#qiskit.algorithms.optimizers.POWELL.gradient_num_diff "qiskit.algorithms.optimizers.POWELL.gradient_num_diff")(x\_center, f, epsilon\[, …]) | We compute the gradient with the numeric differentiation in the parallel way, around the point x\_center. |
| [`optimize`](#qiskit.algorithms.optimizers.POWELL.optimize "qiskit.algorithms.optimizers.POWELL.optimize")(num\_vars, objective\_function\[, …])                   | Perform optimization.                                                                                     |
| [`print_options`](#qiskit.algorithms.optimizers.POWELL.print_options "qiskit.algorithms.optimizers.POWELL.print_options")()                                        | Print algorithm-specific options.                                                                         |
| [`set_max_evals_grouped`](#qiskit.algorithms.optimizers.POWELL.set_max_evals_grouped "qiskit.algorithms.optimizers.POWELL.set_max_evals_grouped")(limit)           | Set max evals grouped                                                                                     |
| [`set_options`](#qiskit.algorithms.optimizers.POWELL.set_options "qiskit.algorithms.optimizers.POWELL.set_options")(\*\*kwargs)                                    | Sets or updates values in the options dictionary.                                                         |
| [`wrap_function`](#qiskit.algorithms.optimizers.POWELL.wrap_function "qiskit.algorithms.optimizers.POWELL.wrap_function")(function, args)                          | Wrap the function to implicitly inject the args at the call of the function.                              |

## Attributes

|                                                                                                                                                                     |                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| [`bounds_support_level`](#qiskit.algorithms.optimizers.POWELL.bounds_support_level "qiskit.algorithms.optimizers.POWELL.bounds_support_level")                      | Returns bounds support level                   |
| [`gradient_support_level`](#qiskit.algorithms.optimizers.POWELL.gradient_support_level "qiskit.algorithms.optimizers.POWELL.gradient_support_level")                | Returns gradient support level                 |
| [`initial_point_support_level`](#qiskit.algorithms.optimizers.POWELL.initial_point_support_level "qiskit.algorithms.optimizers.POWELL.initial_point_support_level") | Returns initial point support level            |
| [`is_bounds_ignored`](#qiskit.algorithms.optimizers.POWELL.is_bounds_ignored "qiskit.algorithms.optimizers.POWELL.is_bounds_ignored")                               | Returns is bounds ignored                      |
| [`is_bounds_required`](#qiskit.algorithms.optimizers.POWELL.is_bounds_required "qiskit.algorithms.optimizers.POWELL.is_bounds_required")                            | Returns is bounds required                     |
| [`is_bounds_supported`](#qiskit.algorithms.optimizers.POWELL.is_bounds_supported "qiskit.algorithms.optimizers.POWELL.is_bounds_supported")                         | Returns is bounds supported                    |
| [`is_gradient_ignored`](#qiskit.algorithms.optimizers.POWELL.is_gradient_ignored "qiskit.algorithms.optimizers.POWELL.is_gradient_ignored")                         | Returns is gradient ignored                    |
| [`is_gradient_required`](#qiskit.algorithms.optimizers.POWELL.is_gradient_required "qiskit.algorithms.optimizers.POWELL.is_gradient_required")                      | Returns is gradient required                   |
| [`is_gradient_supported`](#qiskit.algorithms.optimizers.POWELL.is_gradient_supported "qiskit.algorithms.optimizers.POWELL.is_gradient_supported")                   | Returns is gradient supported                  |
| [`is_initial_point_ignored`](#qiskit.algorithms.optimizers.POWELL.is_initial_point_ignored "qiskit.algorithms.optimizers.POWELL.is_initial_point_ignored")          | Returns is initial point ignored               |
| [`is_initial_point_required`](#qiskit.algorithms.optimizers.POWELL.is_initial_point_required "qiskit.algorithms.optimizers.POWELL.is_initial_point_required")       | Returns is initial point required              |
| [`is_initial_point_supported`](#qiskit.algorithms.optimizers.POWELL.is_initial_point_supported "qiskit.algorithms.optimizers.POWELL.is_initial_point_supported")    | Returns is initial point supported             |
| [`setting`](#qiskit.algorithms.optimizers.POWELL.setting "qiskit.algorithms.optimizers.POWELL.setting")                                                             | Return setting                                 |
| [`settings`](#qiskit.algorithms.optimizers.POWELL.settings "qiskit.algorithms.optimizers.POWELL.settings")                                                          | The optimizer settings in a dictionary format. |

<span id="undefined" />

`property bounds_support_level`

Returns bounds support level

<span id="undefined" />

`get_support_level()`

Return support level dictionary

<span id="undefined" />

`static gradient_num_diff(x_center, f, epsilon, max_evals_grouped=1)`

We compute the gradient with the numeric differentiation in the parallel way, around the point x\_center.

**Parameters**

*   **x\_center** (*ndarray*) – point around which we compute the gradient
*   **f** (*func*) – the function of which the gradient is to be computed.
*   **epsilon** (*float*) – the epsilon used in the numeric differentiation.
*   **max\_evals\_grouped** (*int*) – max evals grouped

**Returns**

the gradient computed

**Return type**

grad

<span id="undefined" />

`property gradient_support_level`

Returns gradient support level

<span id="undefined" />

`property initial_point_support_level`

Returns initial point support level

<span id="undefined" />

`property is_bounds_ignored`

Returns is bounds ignored

<span id="undefined" />

`property is_bounds_required`

Returns is bounds required

<span id="undefined" />

`property is_bounds_supported`

Returns is bounds supported

<span id="undefined" />

`property is_gradient_ignored`

Returns is gradient ignored

<span id="undefined" />

`property is_gradient_required`

Returns is gradient required

<span id="undefined" />

`property is_gradient_supported`

Returns is gradient supported

<span id="undefined" />

`property is_initial_point_ignored`

Returns is initial point ignored

<span id="undefined" />

`property is_initial_point_required`

Returns is initial point required

<span id="undefined" />

`property is_initial_point_supported`

Returns is initial point supported

<span id="undefined" />

`optimize(num_vars, objective_function, gradient_function=None, variable_bounds=None, initial_point=None)`

Perform optimization.

**Parameters**

*   **num\_vars** (*int*) – Number of parameters to be optimized.
*   **objective\_function** (*callable*) – A function that computes the objective function.
*   **gradient\_function** (*callable*) – A function that computes the gradient of the objective function, or None if not available.
*   **variable\_bounds** (*list\[(float, float)]*) – List of variable bounds, given as pairs (lower, upper). None means unbounded.
*   **initial\_point** (*numpy.ndarray\[float]*) – Initial point.

**Returns**

**point, value, nfev**

point: is a 1D numpy.ndarray\[float] containing the solution value: is a float with the objective function value nfev: number of objective function calls made if available or None

**Raises**

**ValueError** – invalid input

<span id="undefined" />

`print_options()`

Print algorithm-specific options.

<span id="undefined" />

`set_max_evals_grouped(limit)`

Set max evals grouped

<span id="undefined" />

`set_options(**kwargs)`

Sets or updates values in the options dictionary.

The options dictionary may be used internally by a given optimizer to pass additional optional values for the underlying optimizer/optimization function used. The options dictionary may be initially populated with a set of key/values when the given optimizer is constructed.

**Parameters**

**kwargs** (*dict*) – options, given as name=value.

<span id="undefined" />

`property setting`

Return setting

<span id="undefined" />

`property settings`

The optimizer settings in a dictionary format.

The settings can for instance be used for JSON-serialization (if all settings are serializable, which e.g. doesn’t hold per default for callables), such that the optimizer object can be reconstructed as

```python
settings = optimizer.settings
# JSON serialize and send to another server
optimizer = OptimizerClass(**settings)
```

**Return type**

`Dict`\[`str`, `Any`]

<span id="undefined" />

`static wrap_function(function, args)`

Wrap the function to implicitly inject the args at the call of the function.

**Parameters**

*   **function** (*func*) – the target function
*   **args** (*tuple*) – the args to be injected

**Returns**

wrapper

**Return type**

function\_wrapper