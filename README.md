# Gradient flow for deep factored scalar linear attention learns multi-step gradient descent

Yitzchak Shmalo

The paper treats in-context learning of scalar linear regression by L untied linear-attention layers, each with a
trainable key scalar and a trainable query scalar. Population gradient flow on the 2L factors is bounded and converges
to a single critical point, and the Hessian has a negative eigenvalue at every critical point that is not a global minimizer. From almost every initialization the
flow reaches a global minimizer. The trained network performs L gradient descent steps whose step sizes are the
reciprocals of the zeros of a rescaled Laguerre polynomial.

- `paper/main.tex`, `paper/main.pdf`: the paper.
- `code/audit_factors.py`: exact rational-arithmetic checks of the moment formula, the normal equations, the risk, the
  flow identities, the saddle Hessians, the exceptional initializations and the separation example. Standard library
  only; run with `python3 code/audit_factors.py`. The proofs do not depend on it.
