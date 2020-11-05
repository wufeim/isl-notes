3.1 Simple Linear Regression
=====================================

*Simple linear regression* assumes that there is approximately a linear relationship between a predictor variable :math:`X` and a quantitative response :math:`Y`, given by

.. math::
  :numbered:

  Y \approx \beta_0 + \beta_1 X

Here, :math:`\beta_0` and :math:`\beta_1` are the coefficients representing the *intercept* and *slope* terms in the linear model.

3.1.1 Estimating the Coefficients
-------------------------------------

Let

.. math::
  :numbered:

  (x_1, y_1), \dots, (x_n, y_n)

represent :math:`n` observation paris. Our goal is to obtain coefficient estimates :math:`\hat{\beta}_0` and :math:`\hat{\beta}_1` such that :math:`y_i \approx \hat{\beta}_0 + \hat{\beta}_1x_i`. Let :math:`\hat{y_i} = \hat{\beta}_0 + \hat{\beta}_1 x_i` be the prediction for :math:`Y` on the :math:`i` th value of :math:`X`. Then :math:`e_i = y_i - \hat{y}_i` represents the :math:`i` th *residual*, and we define the *residual sum of squares* (RSS) as

.. math::
  :numbered:

  \text{RSS} = e_1^2 + \dots + e_n^2

The least squares approach choose :math:`\hat{\beta}_0` and :math:`\hat{\beta}_1` to minimize the RSS. We can show that the minimizers are

.. math::
  :numbered:
  :label: eq3-4

  \hat{\beta}_1 & = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2} \\
  \hat{\beta}_0 & = \bar{y} - \hat{\beta}_1\bar{x}

where :math:`\bar{y}` and :math:`\bar{x}` are the sample means.

3.1.2 Assessing the Accuracy of the Coefficient Estimates

Recall that we assume the *true* relationship between :math:`X` and :math:`Y` takes the form :math:`Y = f(X) + \varepsilon` for some unknown function :math:`f`, where :math:`\varepsilon` is a mean-zero random error term. If :math:`f` is to be approximated by a linear function, then we can write this relationship as

.. math::
  :numbered:
  :label: eq3-5

  Y = \beta_0 + \beta_1 X + \varepsilon

The error term may include the error caused by an inappropriate model, missed variables, or measurement error. We typically assume that the error term is independent of :math:`X`. The model given by :eq:`eq3-5` defines the *population regression line*, and the estimates in :eq:`eq3-4` characterize the *least squares line*.
