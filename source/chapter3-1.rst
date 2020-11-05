3.1 Simple Linear Regression
=====================================

*Simple linear regression* assumes that there is approximately a linear relationship between the predictor variable :math:`X` and the quantitative response :math:`Y`, given by

.. math::

  Y \approx \beta_0 + \beta_1 X

Here, :math:`\beta_0` and :math:`\beta_1` are the coefficients representing the *intercept* and *slope* terms in the linear model.

3.1.1 Estimating the Coefficients
-------------------------------------

Let

.. math::

  (x_1, y_1), \dots, (x_n, y_n)

represent :math:`n` observation paris. Our goal is to obtain coefficient estimates :math:`\hat{\beta}_0` and :math:`\hat{\beta}_1` such that :math:`y_i \approx \hat{\beta}_0 + \hat{\beta}_1x_i`.

Let :math:`\hat{y_i} = \hat{\beta}_0 + \hat{\beta}_1 x_i` be the prediction for :math:`Y` on the :math:`i`th value of :math:`X`. Then :math:`e_i = y_i - \hat{y}_i` represents the :math:`i`th *residual*, and we define the *residual sum of squares* (RSS) ass

.. math::

  \text{RSS} = e_1^2 + \dots + e_n^2
