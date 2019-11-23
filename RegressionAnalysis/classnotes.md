
# Table of Contents

1.  [Session 1 - Summary and Review](#org59569d8)
    1.  [Relationships](#org2c90fc4)
        1.  [Functional](#org6248ee9)
        2.  [Statistical](#orgc65be12)
    2.  [Basic Concepts](#org86957a5)
        1.  [Construction of Regression models](#orga8a4e44)
        2.  [Uses of Regression Analysis](#orgcebde6f)
    3.  [Simple Linear Regression (SLR)](#orgf1df57a)
        1.  [Properties of \(\epsilon_i\)](#orgfac4a41)
        2.  [Properties](#orgc28030e)
        3.  [Alternative forms of SLR](#org1f34974)
        4.  [Method of Least Squares](#org6fcfe7c)
        5.  [Gauss-Markov Theorem](#org2fa99b5)
        6.  [Residual](#orge812183)
    4.  [Normal Error Regression Model](#orgb954f44)
2.  [Session 2 - Inferences in Regression and Correlation Analysis (2019/09/18)](#org9915978)
    1.  [Properties](#org0d915d2)
    2.  [\(\beta_1\)](#orga05eb51)
        1.  [Inferences](#orgf0631d7)
        2.  [Sampling Distribution](#orgb6ac8a7)
        3.  [PROOF: \(b_1\) is a linear combination of Y's](#org9111990)
        4.  [Properties](#org7189d5e)
    3.  [\(\beta_0\)](#org35e100c)
    4.  [Spacing of X Levels](#org7fdd685)
    5.  [Prediction of new observations](#org3e7f816)
        1.  [Interval Estimation of \(E(Y_0)\)](#org7c1c96c)
        2.  [Sampling Distribution](#org7e72e5d)
        3.  [Prediction](#orgf5515c0)
    6.  [ANOVA Approach to Regression](#orga2b5f62)
3.  [Session 3 - General Linear Testing & Model Selection (2019/09/25)](#org21af8f9)
    1.  [General Linear Test Approach](#org91d4fcc)
        1.  [Reduced Model](#orgd9c1b1b)
        2.  [Coefficients of Determination (\(R^2\))](#org1f34ac2)
        3.  [Coefficient of Correlation: \(r = \pm \sqrt{R^2}\)](#org48b0b40)
    2.  [Assessing the Quality of a Model](#org411dca7)
        1.  [Residuals (observed error)](#orgbb6ae20)
        2.  [Residual Plots](#orgcd65446)
        3.  [Test of Randomness](#org08379f4)
        4.  [Constant Variance](#orga4e611b)
4.  [Session 4 - Transformations & Inference (2019/10/02)](#org7d40dcd)
    1.  [Transformations](#orge0ec949)
        1.  [Box-Cox Transformations](#orgf79c1e4)
    2.  [Simultaneous Inference](#org15eee9a)
        1.  [Working-Hotelling Procedure](#orgfbabdfd)
        2.  [Bonferonni Procedure](#org854cbeb)
5.  [Session 5 - Prediction & Linear Algebra in Regression](#orgbd20491)
    1.  [Simultaneous Intervals](#orgb58f983)
        1.  [Confidence](#org8885ee0)
        2.  [Prediction](#orgafd0d1a)
    2.  [Inverse Prediction ("Calibration")](#orgd6d3841)
    3.  [Linear Algebra in Regression](#org7aa5723)
        1.  [Review](#orgcd6a370)
        2.  [Expectations](#orgbbb028a)
        3.  [Variance-Covariance Matrix](#org847273d)
        4.  [Multivariate Normal Distribution](#orgd2bc1d5)
        5.  [Least Squares Estimation](#orgf521527)
6.  [Session 6 - Sums of Squares and Multiple Linear Regression](#org1f8b49e)
    1.  [Sum of Squares](#org40f68c6)
        1.  [SSE](#orgeec8fe5)
        2.  [SSTo](#orgfda62a6)
        3.  [SSR](#org68014fe)
    2.  [Mean Estimates \(\sigma^2\)](#orgc9dd64f)
        1.  [Mean Responses](#orgebbf3a4)
    3.  [Variance of \(\hat{Y_h}\)](#org0965fdd)
    4.  [Multiple Regression Models](#orga98c238)
        1.  [Interpretation](#orge24de43)
        2.  [Aside: Multi-Collinearity](#org1812ba6)
        3.  [Matrix Notation](#org36a3107)
        4.  [ANOVA Table](#orgf0ffece)
        5.  [Omnibus F-Test for Regression Relation](#org3b3489d)
        6.  [Coefficient of Multiple Determination](#org7a723d6)
        7.  [Coefficient of Multiple Correlation](#orgdcb482a)
        8.  [Inferences in \(\beta_k\)](#org862633a)
7.  [Session 7 - Multiple Regression & Qualitative\\/Quantitative Predictors](#org979fa60)
    1.  [Multiple Regression](#orgb7adc46)
        1.  [Extra Sums of Squares](#orgcdc104d)
    2.  [Multi-collinearity](#org4caf32a)
        1.  [Effects](#orgaccaf69)
    3.  [Polynomial Regression Models](#orge0fb7fb)
8.  [Session 8 - Interaction Models & Model Selection](#org42b0744)
    1.  [Interaction Regression Models](#orgee2a372)
        1.  [Additive Effects](#org28d0157)
        2.  [Qualitative Predictors](#orgf20aaec)
    2.  [Model and Variable Selection](#org2ff8ed6)
        1.  [Criterion for Model Selection](#org9bc084b)



<a id="org59569d8"></a>

# Session 1 - Summary and Review


<a id="org2c90fc4"></a>

## Relationships


<a id="org6248ee9"></a>

### Functional

Mathmatical formula

\(Y = f(x)\)


<a id="orgc65be12"></a>

### Statistical

Not a perfect relationship

\(Y = f'(x) + \epsilon\)

observations = trials = case

quadratic = curvilinear

Linear models means that the *slope* is not raised to any powers

-   \(\hat{y} = \beta_0 + \beta_1 X^2\) is linear
-   \(\hat{y} = \beta_0 + \beta_1^2 X\) is **not** linear


<a id="org86957a5"></a>

## Basic Concepts

-   Tendency of Y to vary with X in a *systematic fashion*
-   scatter of points around a curve of a statistical relation
-   Prob. Distr of Y for each **Level** of X
-   means of Y's distr. to vary for each value of X
    -   each point on the regression line can be represented as \(\mu_{Y|X_i}\)

NOTE: Sir Francis Galton came up with the term "regression"

**Regression function of Y on X**: Means of the prob. distr. have a systematic relation to the Level of X

**Regression curve**: graph of the regression function


<a id="orga8a4e44"></a>

### Construction of Regression models

1.  Selection of pred. vars
2.  Functional form of the regression relation
    -   Summary plots
    -   Scatter plots
3.  Scope of Model
    -   **Scope**: What is the Domain? (range of X's)
    -   Making predictions outside the Domain is considered extrapolation and is dangerous


<a id="orgcebde6f"></a>

### Uses of Regression Analysis

1.  Description
2.  Control
3.  Prediction (most abused)

**Association does not imply causation!**


<a id="orgf1df57a"></a>

## Simple Linear Regression (SLR)

\(Y_i = \beta_0 + \beta_1 X_i + \epsilon_i\)

-   One Predictor
-   Linear in the Parameters
-   Linear in the Predictor Variables
-   SLR = First-Order Model (term from outside of statistics)

\(Y_i\): Value of the response for the ith trial
\(\beta_0\): Parameters (unknown. estimate these)
\(X_i\): Value of the predictor of the ith term (known)
\(\epsilon_i\): random error term of the ith observation


<a id="orgfac4a41"></a>

### Properties of \(\epsilon_i\)

-   \(E(\epsilon_i) = 0\)
-   \(\sigma^2(\epsilon_i) = Var(\epsilon_i) = \sigma^2\)
-   \(\epsilon_i\) and \(\epsilon_j\) are uncorrelated


<a id="orgc28030e"></a>

### Properties

1.  \(Y_i\) is the sum of two components. It is **random** because its composed of a
    random term.
    constant term: \(\beta_0 + \beta_1 X_i\)
    random term: \(\epsilon_i\)
2.  \(E(Y_i) = E(\beta_0 + \beta_1 X_i + \epsilon_i)\)
    \(\to E(\beta_0 + \beta_1 X_i) + E(\epsilon_i)\)
    \(\to \beta_0 + \beta_1 X_i\)
3.  \(Y_i\) falls short of regression function by \(\epsilon_i\)
4.  \(Var(\epsilon_i) = \sigma^2\) error terms have constant variance
5.  Since error terms are uncorrelated, then responses (\(Y_i\) and \(Y_j\) are
    uncorrelated)


<a id="org1f34974"></a>

### Alternative forms of SLR

1.  \(Y_i = \beta_0 X_0 + \beta_1 X_i + \epsilon_i\), where \(X_0 = 1\)
2.  \(Y_i = \beta_0 + \beta_1 (X_i - \bar{x}) + \beta_1 \bar{x} + \epsilon_i\)
    \(\to (\beta_0 + \beta_1 \bar{x}) + \beta_1 (x_i - \bar{x}) \epsilon_i\))$
    \(\to \beta_0^* + \beta_1(x_i - \bar{x}) + \epsilon_i\)


<a id="org6fcfe7c"></a>

### Method of Least Squares

1.  Goal

    Find estimators of \(\beta_0\) and \(\beta_1\)
    
    For each \((X_i, Y_i)\): \(Y_i - (\beta_0 + \beta_1 X_i)\)
    \(Q = \sum_{1}^{n} [ Y_i - \beta_0 - \beta_1 X_i ]^2\)
    
    b0 and b1 are estimators of \(\beta_0\) & \(\beta_1\) that minimize Q for given data
    (X<sub>i</sub> Y<sub>i</sub>), i = [1, n]


<a id="org2fa99b5"></a>

### Gauss-Markov Theorem

1.  Proof

    First, lets find the value of \(b_0\) by taking the partial derivative of Q with
    respect to \(\beta_1\)
    
    \begin{proof1}
    Q = \sum_{1}^{n} [Y_i - \beta_{0} - \beta_{1}X_i ]^2
    
    \frac{dQ}{d \beta_{1}} = -2 \sum_{1}^{n} X_i [Y_i - \beta_{0} - \beta_{1} X_i]
    
    \to \sum_{1}^{n} X_i (Y_i - b0 -b1 X_i) = 0
    
    \to \sum_{1}^{n} X_i Y_i - b_0 \sum_{1}^{n} x_i - b_1 \sum_{1}^{n} x_i^2 = 0
    
    \to \sum_{1}^{n} Y-i - n b_0 - b_1 \sum_{1}^{n} x_i = 0
    
    \to \sum_{1}^{n} Y_i - b_1 \sum_{1}^{n} x_i = nb_0
    
    \to \bar{Y} - b_1 \bar{x} = b_0
    \end{proof1}
    
    Once \(b_0\) is found, lets use it to find the value of \(b_1\). Replace
    values of \(b_0\) with the equation above.
    
    \begin{proof2}
    
    \sum_{1}^{n} X_i Y_i - b_0 \sum_{1}^{n} x_i - b_1 \sum_{1}^{n} x_i^2 = 0
    
    \to \sum_{1}^{n} X_i Y_i - (\bar{Y} - b_1 \bar{x}) \sum_{1}^{n} x_i - b_1 \sum_{1}^{n} x_i^2 = 0
    
    \to \sum_{1}^{n} X_i Y_i - (\frac{\sum_{1}^{n} Y_i}{n} - b_1 \frac{\sum_{1}^{n} x_i}{n}) \sum_{1}^{n} x_i - b_1 \sum_{1}^{n} x_i^2 = 0
    
    \to \sum_{1}^{n} X_i Y_i - \frac{\sum_{1}^{n} x_i \sum_{1}^{n} y_i}{n} + b_1 \frac{(\sum_{1}^{n} x_i)^2}{n} - b_1 \sum_{1}^{n} x_i^2
    
    \to \sum_{1}^{n} x_i y_i - \frac{\sum_{1}^{n} x_i \sum_{1}^{n} y_i}{n} = b_1 [ \sum_{1}^{n} x_i^2 - \frac{(\sum_{1}^{n} x_i)^2}{n} ]
    
    = ... = \frac{\sum_{1}^{n} (x_i - x)(y_i - \bar{y})}{\sum_{1}^{n} (x_i - \bar{x})^2}
    \end{proof2}

2.  Properties

    1.  \(E(b0) = \beta_0\) & \(E(b1) = \beta_1\)
    2.  b0 & b1 are more precise than any other unbiased estimators of \(\beta_0\) and
        \(\beta_1\) that are linear functions of \(Y_i\)


<a id="orge812183"></a>

### Residual

Difference between the observation and the estimated value
\(\e_i  = Y_i - \hat{Y_i}\), i == [1, n]

1.  \(\sum_{i}^{n} e_i = 0\)
2.  \(\sum_{i}^{n}e_i^2\) is a minimum
3.  \(\sum_{i}^{n}Y_i = \sum_{i}^{n} \hat{Y_i}\)

1.  Goal

    Estimate \(\sigma^2\)
    know \(E(S^2) = E(\frac{\sum(Y_i - \bar{Y})^2}{n - 1})\)
    
    -   numerator == sum of squares
    -   n - 1 == df
    -   \(S^2\) = Mean Square = \(\frac{SS}{df}\)

2.  SSE

    SSE = \(\sum(Y_i - \hat{Y_i})^2 = \sum e_i^2\)
    
    -   SSE = Sum of Square Error = Residual Sums of Squares
    -   MSE = SSE / n - 2
    -   df of SSE = n - 2
    -   E(MSE) = \(\sigma^2\)


<a id="orgb954f44"></a>

## Normal Error Regression Model

\(Y_i = \beta_0 + \beta_1 X_i + \epsilon_i\)
where
\(\epsilon \approx iid N(0,\sigma^2)\), i = [1, n]
so
\(Y_i \approx N(\beta_0 + \beta_1 X_i, \sigma^2)\)
To find MLE's of \(\beta_0\) & \(\beta_1\) i.e. \(\hat{\beta_0}\) & \(\hat{\beta_1}\)
\(L(\beta_0, \beta_1m \sigma^2) =\prod pdf\)

-   MLE of \(\beta_0\): \(\hat{\beta_0} = b_0\)
-   MLE of \(\beta_1\): \(\hat{\beta_1} = b_1\)


<a id="org9915978"></a>

# Session 2 - Inferences in Regression and Correlation Analysis (2019/09/18)

Model = \(Y_i = \beta_0 \beta_1 X_i + \epsilon_i\)


<a id="org0d915d2"></a>

## Properties

-   \(\epsilon_i \approx iid N(0, \sigma^2)\)
-   \(Y_i \approx iid N(\beta_0 + \beta_1 X_i, \sigma^2)\)
-   \(X_i\): known constant
-   \(\beta_0\) & \(\beta_1\) are parameters to investigate


<a id="orga05eb51"></a>

## \(\beta_1\)


<a id="orgf0631d7"></a>

### Inferences

\(H_0: \beta_1 = 0\) (implies no linear association)
\(H_1: \beta_1 \neq 0\)

This hypothesis test determines if there is a relationship


<a id="orgb6ac8a7"></a>

### Sampling Distribution

\(b_1 = \frac{\Sigma((x_i - \bar{x})(y_i - \bar{y} ))}{\Sigma(x_i - \bar{x})^2}\)

-   \(E(b_1) = \beta_1\)
-   \(Var(b_1) = \frac{\sigma^2}{\Sigma(x_i - \bar{x})^2}\)


<a id="org9111990"></a>

### PROOF: \(b_1\) is a linear combination of Y's

-   \(b_1 = \frac{\Sigma((x_i - \bar{x})(y_i - \bar{y} ))}{\Sigma(x_i - \bar{x})^2}\)
-   \(b_1 = \frac{\Sigma((x_i - \bar{x}) y_i - \bar{y} \Sigma(x_i - \bar{x})}{\Sigma(x_i - \bar{x})^2}\)
-   \(b_1 = \frac{\Sigma((x_i - \bar{x}) y_i}{\Sigma(x_i - \bar{x})^2}\)

Let \(K_i = \frac{x_i - \bar{x}}{\Sigma(x_i - \bar{x})^2}\)

**Facts about \(K_i\)**

-   \(\Sigma{K_i} = \Sigma \frac{x_i - \bar{x}}{\Sigma (X_i - \bar{x})^2} = 0\)
-   \(\Sigma K_i^2 = \Sigma (\frac{x_i - \bar{x}}{\Sigma (X_i - \bar{x})^2)^2} = \frac{1}{\Sigma{(x_i - \bar{x})^2}}\)

-   \(b_1 = \Sigma K-i Y_i\)

Therefore \(b_1\) is a linear combination of Y<sub>i</sub>


<a id="org7189d5e"></a>

### Properties

-   \(E(\hat{\beta_1}) = E(\Sigma K_i Y_i) = \Sigma K_i E(Y_i) = \Sigma K_i
      (\beta_0 + \beta_1 X_i) = \beta_1 \Sigma K_i X_i = \beta_1\)

More detailed proof of \(\Sigma K_i X_i = 1\) exists in notes. It was a sidebar in
class.

-   \(\beta_1 \approx N(\beta_1, \frac{\sigma^2}{\Sigma(x_i - \bar{x})^2})\)
-   \(\frac{b_1 - \beta_1}{\sqrt{\frac{\sigma^2}{\Sigma(x_i - \bar{x})^2}}} \approx
      N(0,1)\)

Recall E(MSE) = \(E(\frac{SSE}{n - 2}) = \sigma^2\)

Thus \(\frac{b_1 - \beta_1}{\sqrt{\frac{MSE}{\Sigma(x_i - \bar{x})^2}}} \approx
  t_{n-2}\)
NOTE: a T Distribution is a standard normal distribution divided by a chi-square
  distribution scaled by its DF

1.  Solving the Hypothesis Test

    Recall
    
    \(H_0: \beta_1 = 0\)
    \(H_1: \beta_1 \neq 0\)
    
    **Test Statistic**
    
    \(t* = \frac{b_1}{\sqrt{\frac{MSE}{\Sigma(x_i - \bar{x})^2}}} =
    \frac{b_1}{SE_{b1}} \approx t_{n - 2}\)
    
    Then p-value can be calculated


<a id="org35e100c"></a>

## \(\beta_0\)

\(b_0 \approx N(\beta_0, \sigma^2[\frac{1}{n} + \frac{\bar{x}^2}{\Sigma (x_i - \bar{x})^2}])\)

If \(Y_i\) are not exactly normal, \(b_0\) and \(b_1\) are approx. normal. Thus the t
statistic provides some level of confidence.


<a id="org7fdd685"></a>

## Spacing of X Levels

-   The greater the spread of x, the larger \(\Sigma (x_i - \bar{x})^2\)
-   Var(\(b_1\)) and Var(\(b_0\)) decrease


<a id="org3e7f816"></a>

## Prediction of new observations

Let a new observation be defined as \(Y_0\)


<a id="org7c1c96c"></a>

### Interval Estimation of \(E(Y_0)\)

-   \(X_0\): level of x we want to estimate the mean response
-   \(E(Y_0)\): mean response when \(X = X_0\)
-   \(\hat{Y_0} = b_0 + b_1 X_0\): Point estimate of \(E(Y_0)\)


<a id="org7e72e5d"></a>

### Sampling Distribution

\(\hat{Y_0} \approx N(E(Y_0), \sigma^2 [\frac{1}{n} + \frac{(x_0 - \bar{x})^2}{\Sigma
(x_i - \bar{x})^2}])\)

\(\hat{Y_0} \pm t_{\frac{\alpha}{2}, n - 2} \sqrt{MSE (\frac{1}{n} + \frac{(X_0 -
\bar{x})^2}{\Sigma (x_i - \bar{x})^2})}\)

NOTE:
**confidence interval == mean**
**prediction interval == single value**


<a id="orgf5515c0"></a>

### Prediction

\(\hat{Y_1}\): predicted individual outcome drawn from the distr. of \(Y\)

**Assumptions**

-   \(E(Y_1)\): estimated by \(\hat{Y_1}\)
-   Var(\(Y_1\)): estimated by MSE

\(Var(pred) = Var(\hat{Y_1}) + Var(\hat{Y_0}) = \sigma^2 [ 1 + \frac{1}{n} +
\frac{(x_0 - \bar{x})^2}{\Sigma (x_i - \bar{x})^2}]\)

**100(\(1 - \alpha\))% Prediction Interval**

-   \(\hat{Y_1} \pm t_{\frac{\alpha}{2}, n - 2} \sqrt{MSE (1 + \frac{1}{n} +
      \frac{(x_0 - \bar{x})^2}{\Sigma (x_i - \bar{x})^2})}\)


<a id="orga2b5f62"></a>

## ANOVA Approach to Regression

Partition the Total Sums of Squares

1.  When ignoring the predictor variable, Variation is based on \(Y_i - \bar{Y}\)
    deviations.
    
    \(SSTo\): Total Sums of Squares (or TSS)
    Therefore, \(SSTo = \Sigma(Y_i - \bar{y})^2\)

2.  When using the predictor variable, variation based on \(Y_i - \hat{Y_i}\)
    deviations. i.e. residuals
    
    \(SSE\): Error Sum of Squares
    Therefore, \(SSE = \Sigma(Y_i - \hat{Y_i})^2\)

\(SSR\): Regression Sum of Squares
\(SSR = \Sigma (Y_i - \bar{y})^2\)

**NOTE**: SSR = SSTo - SSE **OR** SSTo = SSR + SSE. proof is in notebook. record
here if needed

**Degrees of Freedom (df)**

-   SSto: n - 1. \(Y_i - \bar{y}\)
-   SSE: n - 2. \(Y_i - \hat{Y_i}\)
-   SSR: 2 - 1 = 1. \(\hat{Y_i} - \bar{y}\)

NOTE:

-   \(E(MSE) = \sigma^2\)
-   \(E(MSR) = \sigma^2 + \beta_1^2 \Sigma (x_i - \bar{x})^2\)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Source</th>
<th scope="col" class="org-left">SS</th>
<th scope="col" class="org-left">df</th>
<th scope="col" class="org-left">MS</th>
<th scope="col" class="org-left">F Statistic</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Regression</td>
<td class="org-left">SSR</td>
<td class="org-left">1</td>
<td class="org-left">\(MSR = \frac{SSR}{1}\)</td>
<td class="org-left">\(F = \frac{MSR}{MSE}\)</td>
</tr>


<tr>
<td class="org-left">Error</td>
<td class="org-left">SSE</td>
<td class="org-left">n - 2</td>
<td class="org-left">\(MSE = \frac{SSE}{n - 2}\)</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">**Total**</td>
<td class="org-left">SSTo</td>
<td class="org-left">n - 1</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>

\(F*\) is the test statistic for

\(H_0: \beta_1 = 0\)
\(H_1: \beta_1 \neq 0\)

\(F* \approx F_{1, n-2}\) if \(H_0\) is true
\((t*)^2 = F*\) if \(F* \approx F_{1, n - 2}\)


<a id="org21af8f9"></a>

# Session 3 - General Linear Testing & Model Selection (2019/09/25)


<a id="org91d4fcc"></a>

## General Linear Test Approach

Full Model: \(Y_i = \beta_0 + \beta_1 X_i + \epsilon_i\) where \(\epsilon_i \approx
iid N(0, \sigma^2)\)

This can be fit by either <span class="underline">Least Squares</span> or <span class="underline">Maximum Likelihood</span>

**Notes**
F `= Full Model
R =` Reduced Model

\begin{equation}
\begin{split}
SSE(F) & = \Sigma [ Y_i - (b_0 + b_1 X_i) ]^2 \\
& = \Sigma{ (Y_i - \hat{Y_i})^2} \\
& = SSE
\end{split}
\end{equation}


<a id="orgd9c1b1b"></a>

### Reduced Model

\begin{equation}
\begin{split}
H_0: \beta_1 = 0 & \text{ if $H_0$ then $Y_i = \beta_0 + \epsilon_i$} \\
H_A: \beta_1 \neq 0 &
\end{split}
\end{equation}

**Test Statistic**: \(SSE(F) \leq SSE(R)\)

The more parameters in the model, the better the fit **thus** smaller deviations
around the fitted regression model.

A small diff suggests \(H_0\) holds. (\(SSE(R) - SSE(F)\))

\begin{equation}
\begin{split}
F^* = \frac{\frac{SSE(R) - SSE(F)}{df_R - df_F}}{\frac{SSE(F)}{df_F}}
\end{split}
\end{equation}

**Note**: The full model has less variation because the hope is that the predictor
 (X) helps explain the spread in the response (Y).

p-value = \(P(F_{df_R - df_F, df_F} \geq F^*)\)
For SLR and testing the null hypothesis (\(H_0: \beta_1 = 0\)),

\begin{equation}
\begin{split}
F^* & = \frac{\frac{SSTo - SSE}{(n - 1) - (n - 2)}}{\frac{SSE}{n - 2}}\\
& = \frac{SSR}{MSE}\\
& = \frac{MSR}{MSE}
\end{split}
\end{equation}

This is exactly like the ANOVA table!


<a id="org1f34ac2"></a>

### Coefficients of Determination (\(R^2\))

**Goal**: Quantify how much variation in the repsonse is explained by the model.
**Def**: The proportion of variation in Y explained by regressing Y on X.

\(R^2 =\frac{SSR}{SSTo} = 1 - \frac{SSE}{SSTo}\)

**Properties**

-   \(0 \leq R^2 \leq 1\)
-   \(R^2 = 1\) indicates a perfect fit
-   \(R^2 = 0 \to b_1 = 0\) thus a horizontal line **OR** a non-linear pattern

A high \(R^2\) value does <span class="underline">NOT</span> indicate

-   useful predictions can be made
-   estimated regression line is a good fit
-   x and y are related


<a id="org48b0b40"></a>

### Coefficient of Correlation: \(r = \pm \sqrt{R^2}\)

A measure of the linear association between Y and X when Y and X are random variables.
**Properties**

-   \(-1 \leq r \leq 1\)
-   sign of correlation matches sign of slope


<a id="org411dca7"></a>

## Assessing the Quality of a Model

**Diagnostics for X (predictor variable)**

1.  Dot Plot
2.  Sequence Plot
    \(X_1, ..., X_n\). No pattern is good
3.  Stem-and-Leaf plot (< 100 observations)
4.  Box Plot
5.  Histogram


<a id="orgbb6ae20"></a>

### Residuals (observed error)

\(\e_i = Y_i \hat{Y_i}\)

**Properties**

-   \(\bar{e} = \frac{\Sigma e_i}{n} = 0\)
-   \(S^2_e = \frac{\Sigma (e_i - \bar{e})^2}{n - 2} = \frac{\Sigma e_i^2}{n - 2} =
      \frac{SSE}{n - 2} = MSE\)
-   \(e_i\)'s are **not** independent random variables.
    -   If large n, the dependence of \(e_i\) is relatively unimportant and can be
        ignored

**Standardized vs Studentized**

-   Standardized = \(\frac{Y_i - \bar{y}}{\sigma}\)
-   Studentized = \(\frac{Y_i - \mu}{\frac{\sigma}{n}}\)

**Semi-studentized Residuals**
\(e_i^* =\frac{e_i - \bar{e}}{\sqrt{MSE}} =\frac{e_i}{\sqrt{MSE}}\)


<a id="orgcd65446"></a>

### Residual Plots

Residual Plot Form

![img](./images/empty_res-1.jpg "Empty Residual Plot")

1.  Tests

    1.  Non-linearity of regression function
        A pattern indicates linear regression not appropriate
    
    ![img](./images/resplot_1-1.jpg "Plots 1")
    
    1.  Non-constancy of error terms
        Fanning indicates different variances for different values of \(X_i or \hat{Y_i}\)
        
        ![img](./images/resplot_2-1.jpg "Plots 2")
    2.  Presence of outliers
        Graph Semi-studentized residuals on a Residual plot **OR** a Box Plot
        
        ![img](./images/resplot_3-1.jpg "Plots 3")
        if \(\abs{E_i^*} \geq 4\), outlier
    3.  Non-independence of error terms (more of a concern with time-series)
        No pattern is good. Error terms safe to assume independent.
        
        ![img](./images/resplot_4-1.jpg "Plots 4")
    4.  Normality of Error Terms
        -   Use a normal probability plot. The closer the points the fall on a straight
            line, the closer they are to a normal distribution.
            
            ![img](./images/resplot_5-1.jpg "Plots 5")
    5.  Omission of Important Predictors?
        A Pattern indicates that there might be a relationshup between the residuals
        and some other predictor. This can be used to determine whether a predictor
        shoudl be used <span class="underline">before</span> modeling it. Probably not as necessary anymore since
        it is easy to run and compare models.


<a id="org08379f4"></a>

### Test of Randomness

1.  Durbin-Watson Test

    \begin{equation}
    \begin{split}
    H_0: \phi = 0 & \text{where $\phi$ is an autocorrelation coefficient} \\
    H_A: \phi \gt 0 & \text{most assume positive correlation}
    \end{split}
    \end{equation}
    
        lmtest::dwtest(modle)

2.  Shapiro-Wilk Test for Normality

    Not writing much here because I know it already
    
        shapiro.test()


<a id="orga4e611b"></a>

### Constant Variance

1.  Brown-Forsyth Test

    Robust since it uses Median
    
        lawstat::levene.test()

2.  Breusch-Pagan Test

    Sensitive to departures from Normality
    
    \(log(\sigma^2) = \gamma_0 + \gamma_1 x_i\)
    
    \begin{equation}
    \begin{split}
    H_0: \gamma_1 = 0\\
    H_A: \gamma_1 \neq 0
    \end{split}
    \end{equation}
    
        lmtest::bptest()
    
    **NOTES**: Heteroscedascity means non-constant variance


<a id="org7d40dcd"></a>

# Session 4 - Transformations & Inference (2019/10/02)


<a id="orge0ec949"></a>

## Transformations

If non-normality and unequal error variance:

1.  Transform Y: \(Y' = f(Y)\)
2.  Transform X: \(X' = f(X)\)

If non-linearity (rarer)

1.  Transform X: \(X' = f(X)\)

In order to determine which transformation to choose, look at the raw data and
make a judgement call.

<span class="underline">In Class Example</span>

\(Y_i' = log(Y_i) = \beta_0 + \beta_1 X_i + \epsilon_i \equiv Y_i = exp(\beta_0 +
\beta_1 X_i + \epsilon_)i\)

A 1 unit increase in X is associated with a \(exp(\beta_1)\) multiplicative effect
on the **geometric** mean. This [link](https://stats.idre.ucla.edu/other/mult-pkg/faq/general/faqhow-do-i-interpret-a-regression-model-when-some-variables-are-log-transformed/) explains in detail the impact of log
transformed variables.

Geometric mean = \((\Pi x_i)^\frac{1}{n}\)

\(\hat{Y_i} = log(Y)\)

\(X_i' = \sqrt{x}\)

\(\hat{Y_i} = 4.896 + 4.325 X_i' \to exp(4.235) = 75.528\)

For each 1 unit increase in \(X'\), the estimated increase in the geometric mean
price is 75.53 times its previous value.


<a id="orgf79c1e4"></a>

### Box-Cox Transformations

There is a value \(\lambda\) that is the optimal transformation to the response
for equal variance and normality. It is optimal in the sense that it finds the
value of \(\lambda\) which produces the smallest SSE for \(Y_i\).

\(Y_i^{\lambda} = \beta_0 + \beta_1 X_i + \epsilon_i \text{where} i \sim
\text{iid } N(0,
\sigma^2)\)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-right" />

<col  class="org-right" />

<col  class="org-right" />

<col  class="org-right" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">\(\lambda\)</th>
<th scope="col" class="org-right">2</th>
<th scope="col" class="org-right">0.5</th>
<th scope="col" class="org-right">0</th>
<th scope="col" class="org-right">-0.5</th>
<th scope="col" class="org-right">-1</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">\(Y' = Y^{\lambda}\)</td>
<td class="org-right">\(Y^2\)</td>
<td class="org-right">\(\sqrt{Y}\)</td>
<td class="org-right">log(Y)</td>
<td class="org-right">\(\frac{1}{\sqrt{Y}}\)</td>
<td class="org-right">\(\frac{1}{Y}\)</td>
</tr>
</tbody>
</table>

    lindia::gg-boxcox(model)


<a id="org15eee9a"></a>

## Simultaneous Inference

**Goal**: Try to estimate more than one mean response at a time.

\((0.95)^3 = 0.857375\)


<a id="orgfbabdfd"></a>

### Working-Hotelling Procedure

Based on the confidence band for the regression line.

100(1 - \(\alpha\))% simultanous confidence limits for g mean responses \(E(Y_h)\)

\(Y_h \pm W \sqrt{MSE(\frac{1}{n} +\frac{(X_h - \bar{X})^2}{\Sigma(X_i - \bar{X})^2})} \text{where } W^2 = 2 F_{1- \alpha, 2, n - 2}\)

    qf(1 - $\alpha$, 2, n - 2)


<a id="org854cbeb"></a>

### Bonferonni Procedure

\(Y_h \pm B \sqrt{MSE(\frac{1}{n} + \frac{(X_h - \bar{X})^2}{\Sigma(X_i - \bar{X})^2}
)} \text{where } B = t_{1 -\frac{\alpha}{2g}, n - 2}\)

    qt(1 - alpha / 2g, n - 2)


<a id="orgbd20491"></a>

# Session 5 - Prediction & Linear Algebra in Regression


<a id="orgb58f983"></a>

## Simultaneous Intervals


<a id="org8885ee0"></a>

### Confidence

Using the Bonferonni adjustment, The simultanous confidence interval for mean winning percentage for RunDiff of
\(X_h = -100,0,100\) has a confidence level = \(1 - \frac{\alpha}{g}\) where \(\alpha
= .05\) and \(g = 3\)

This is good for a smaller number of predictors. i.e. \(g < 10\)


<a id="orgafd0d1a"></a>

### Prediction

**Bonferroni**: \(\hat{Y_h} \pm t_{1 -\frac{\alpha}{2g}, n-2}
\sqrt{\text{MSE}(1 + \frac{1}{n} +\frac{(x_h - \bar{x})^2}{\Sigma(x_i - \bar{x})^2})}\)
level = \(1 - \frac{\alpha}{g}\)

**Scheffe**: \(\hat{Y_h} \pm S \sqrt{\text{MSE}(1 + \frac{1}{n} +\frac{(x_h -
 \bar{x})^2}{\Sigma(x_i - \bar{x})^2})}\) where \(S = \sqrt{g F_{1 - \alpha,g,n-2}}\)

Scheffe is more efficient with a larger **g** (i.e. g > 10). An in-class example
showed that this was not the case so the jury is still out.


<a id="orgd6d3841"></a>

## Inverse Prediction ("Calibration")

First, construct a model where \(Y = X\)

<span class="underline">Goal</span>: Make a prediction of X that was used to predict a new value of Y.

\begin{equation}
\begin{split}
\hat{Y_i} & = \beta_0 + \beta_1 X_i + \epsilon_i \text{ where } \epsilon_i \sim \text{ iid } N(0, \sigma^2)\\
\hat{Y} & = b_0 + b_1 x
\end{split}
\end{equation}

We are given \(Y_{h(new)}\), so what is \(X_{h(new)}\)?

\(\hat{X_h(new)} = \frac{Y_{h(new)} - b_0}{b_1}\)

\(\hat{X_{h(new)}} \pm t_{1 - \frac{\alpha}{2},n-2} \sqrt{\frac{MSE}{b_1^2} (1 + \frac{1}{n} +\frac{(x_{h(new)} - \bar{x})^2}{\Sigma(x_i - \bar{x})^2})}\)

    investr::calibrate(model, Y, interval = "Wald")

The approximate confidence interval is appropriate if the following quantity is
small (i.e. < .1):

\(\frac{t_{1 - \frac{\alpha}{2}, n - 2}^2 MSE}{b_1^2 \Sigma (X_i - \bar{X})^2}\)


<a id="org7aa5723"></a>

## Linear Algebra in Regression


<a id="orgcd6a370"></a>

### Review

\(\underset{(n X 1)}{\vec{Y}} =
\begin{bmatrix}
Y_1\\
Y_2\\
...\\
Y_n
\end{bmatrix}\)

\(\underset{(1 \times n)}{\vec{Y^T}} = \begin{bmatrix}
Y_1 & ... & Y_n
\end{bmatrix}\)

**Design Matrix**

\(\underset{(n \times 2)}{X} = \begin{bmatrix}
1 & x_1\\
1 & x_2\\
... & ...\\
1 & x_n
\end{bmatrix}\)

\(\underset{(2 \times n)}{x^T} = \begin{bmatrix}
1 & ... & 1\\
x_1 & ... & x_n
\end{bmatrix}\)

1.  Matrix Addition & Subtraction

    \begin{equation}
    \begin{split}
    Y_i = & E(Y_i) + \epsilon_i\\
    \vec{Y} = & E(\vec{Y}) + \vec{\epsilon}\\
    E(\vec{Y}) = & \begin{bmatrix}
    E(Y_1)\\
    ...\\
    E(Y_n)
    \end{bmatrix}\\
    \vec{\epsilon{}} = & \begin{bmatrix}
    \epsilon_1\\
    ...\\
    \epsilon_n
    \end{bmatrix}
    \end{split}
    \end{equation}

2.  Matrix Multiplication

    \begin{equation}
    \begin{split}
    \underset{(1 \times n)(n \times 1)}{\vec{Y}^T \vec{Y}} = & \begin{bmatrix}
    Y_1 & ... & Y_n
    \end{bmatrix}\begin{bmatrix}
    Y_1\\
    ...\\
    Y_n
    \end{bmatrix} = \sum_{1}^{n}Y_i^2\\
    \underset{(2 \times n)(n \times 2)}{X^T X} = & \begin{bmatrix}
    1 & ... & 1\\
    x_1 & ... & x_n
    \end{bmatrix} \begin{bmatrix}
    1 & x_1\\
    ... & ...\\
    1 & x_n
    \end{bmatrix} = \begin{bmatrix}
    n & \Sigma X_i\\
    \Sigma X_i & \Sigma X_i^2
    \end{bmatrix}\\
    \underset{(2 \times n)(n \times 1)}{X^T \vec{Y}} = & \begin{bmatrix}
    1 & ... & 1\\
    x_1 & ... & x_n
    \end{bmatrix} \begin{bmatrix}
    Y_1\\
    ...\\
    Y_n
    \end{bmatrix} = \begin{bmatrix}
    \Sigma Y_i\\
    \Sigma X_iY_i
    \end{bmatrix}
    \end{split}
    \end{equation}

3.  Special Matrices

    **Symmetric**: \(A = A^T\)
    This implies a square matrix. i.e. n x n
    
    **Diagonal**: \(\underset{(n \times n)}A = \begin{bmatrix}
    a_{11} & 0 & ... & 0\\
    0 & a_{22} & ... & 0\\
    ... & ... & ... & ...\\
    0 & 0 & 0 & a_{nn}
    \end{bmatrix}\)
    
    **Identity Matrix**: \(\underset{(n \times n)}I = \begin{bmatrix}
    1 & ... & 0\\
    ... & 1 & ...\\
    0 & ... & 1
    \end{bmatrix}\)
    
    **Scalar**: \(gI = \begin{bmatrix}
    g & ... & 0\\
    ... & g & ...\\
    0 & ... & g
    \end{bmatrix}\) where \(g\) is a scalar value
    
    **One vectors**
    
    \begin{equation}
    \begin{split}
    \underset{(n \times 1)}{\vec{1}} = & \begin{bmatrix}
    1\\
    ...\\
    1
    \end{bmatrix}\\
    \underset{(n \times n)} J = & \begin{bmatrix}
    1 & ... & 1\\
    ... & 1 & ...\\
    1 & ... & 1
    \end{bmatrix}\\
    \underset{(1 \times n)(n \times 1)}{\vec{1}^T \vec{1}} = & n\\
    \underset{(n \times 1)(1 \times n)}{\vec{1} \vec{1}^T} = & \begin{bmatrix}
    1\\
    ...\\
    1
    \end{bmatrix} \begin{bmatrix}
    1 & ... & 1
    \end{bmatrix} = J
    \end{split}
    \end{equation}

4.  Inverse of a Matrix

    \begin{equation}
    \begin{split}
    \underset{(2 \times 2)}{A} = &\begin{bmatrix}
    a & b\\
    c & d
    \end{bmatrix}\\
    \underset{(2 \times 2)}{A^-1} = & \frac{1}{det(A)} \begin{bmatrix}
    d & -b\\
    -c & a
    \end{bmatrix} = \frac{1}{ad - bc} \begin{bmatrix}
    d & -b\\
    -c & a
    \end{bmatrix}
    \end{split}
    \end{equation}
    
    **Application to Regression**
    
    \begin{equation}
    \begin{split}
    \underset{2 \times 2}{(X^T X)^-1} = & \frac{1}{det(X^T X)} \begin{bmatrix}
    \Sigma x_i^2 & - \Sigma x_i\\
    - \Sigma x_i & n
    \end{bmatrix} = ... = \begin{bmatrix}
    \frac{\Sigma x_i^2}{n \Sigma (x_i - \bar{x})^2} & - \frac{\Sigma x_i}{n \Sigma (x_i - \bar{x})^2}\\
    - \frac{\Sigma x_i}{n \Sigma (x_i - \bar{x})^2} & \frac{n}{n \Sigma (x_i - \bar{x})^2}
    \end{bmatrix}\\
    det(X^T X) = & n \Sigma x_i^2 - (\Sigma x_i)^2\\
    & = n \Sigma x_i^2 - \frac{n (\Sigma x_i)^2}{n^2}\\
    & = n [ \Sigma x_i^2 - \frac{(\Sigma x_i)^2}{n}]\\
    & = n \Sigma (x_i - \bar{x})^2
    \end{split}
    \end{equation}
    
    **Side Note**
    
    \begin{equation}
    \begin{split}
    \Sigma x_i = & n \bar{x}\\
    \Sigma (x_i - \bar{x})^2 = & \Sigma x_i^2 - n \bar{x}^2\\
    \Sigma x_i^2 = & \Sigma (x_i - \bar{x})^2 + n \bar{x}^2\\
    (X^T X)^-1 = & \begin{bmatrix}
    \frac{1}{n} + \frac{\bar{x}^2}{\Sigma (x_i - \bar{x})^2} & - \frac{\bar{x}}{\Sigma (x_i - \bar{x})^2}\\
    - \frac{\bar{x}}{\Sigma (x_i - \bar{x})^2} & \frac{1}{\Sigma (x_i - \bar{x})^2}
    \end{bmatrix}
    \end{split}
    \end{equation}

5.  Matrix Rules

    \begin{equation}
    \begin{split}
    A + B = & B + A\\
    (A + B) + C = & A + (B + C)\\
    (AB)C = & A(BC)\\
    C(A + B) = & CA + CB\\
    \\
    (A^T)^T = & A\\
    (A + B)^T = & A^T + B^T\\
    (AB)^T = & B^T A^T\\
    \\
    (AB)^{-1} = & B^{-1} A^{-1}\\
    (A^-1)^{-1} = & A\\
    (A^T)^{-1} = & (A^{-1})^T
    \end{split}
    \end{equation}


<a id="orgbbb028a"></a>

### Expectations

\begin{equation}
\begin{split}
\underset{(n \times 1)}{\vec{Y}} = & \begin{bmatrix}
Y_1\\
...\\
Y_n
\end{bmatrix}\\
\underset{(n \times 1)}{E(\vec{Y})} = & \begin{bmatrix}
E(Y_1)\\
...\\
E(Y_n)
\end{bmatrix}\\
\vec{\epsilon} = & \begin{bmatrix}
\epsilon_1\\
...\\
\epsilon_n
\end{bmatrix}\\
E(\vec{\epsilon}) = & \vec{0}
\end{split}
\end{equation}


<a id="org847273d"></a>

### Variance-Covariance Matrix

\begin{equation}
\begin{split}
\sigma^2(\vec{Y}) = & \begin{bmatrix}
Var(Y_i) & ... & Cov(Y_1, Y_n)\\
... & ... & ...\\
Cov(Y_n, Y_1) & ... & Var(Y_n)
\end{bmatrix}
\end{split}
\end{equation}

When \(Y_i\) independent, the off diagonals are 0 meaning \(\sigma^2(\vec{Y}) =
\sigma^2 I\)
**Aside**

\begin{equation}
\begin{split}
Var(Y) = & E[ (Y - E(Y))^2 ]\\
\sigma^2(\vec{Y}) = & E [ (\vec{Y} - E(\vec{Y}))(\vec{Y} - E(\vec{Y}))^T ]
\end{split}
\end{equation}

Let \(\underset{(p \times 1)}{\vec{W}} = \underset{(p \times n)(n \times 1)}{A
\vec{Y}}\) where A is a matrix of **constants** and Y is a **random vector**

\begin{equation}
\begin{split}
E(A) = & A\\
E(\vec{W}) = & AE(\vec{Y})\\
\sigma^2(\vec{W}) = & E[ (\vec{W} - E(\vec{W}))(\vec{W} - E(\vec{W}))^T ]\\
= & E[ (A \vec{Y} - AE(\vec{Y}))(A \vec{Y} - A E(\vec{Y}))^T ]\\
= & E[ A(\vec{Y} - E(\vec{Y}))(A(\vec{Y} - E(\vec{Y}))^T ]\\
= & E[ A(\vec{Y} - E(\vec{Y}))(\vec{Y} - E(\vec{Y}))^T A^T]\\
= & A E[ (\vec{Y} - E(\vec{Y}))(\vec{Y} - E(\vec{Y}))^T ] A^T\\
= & A \sigma^2(\vec{Y}) A^T
\end{split}
\end{equation}


<a id="orgd2bc1d5"></a>

### Multivariate Normal Distribution

\begin{equation}
\begin{split}
\underset{(p \times 1)}{\vec{Y}} = & \begin{bmatrix}
Y_1\\
...\\
Y_p
\end{bmatrix}\\
\underset{(p \times 1)}{\vec{\mu}} = & \begin{bmatrix}
\mu_1\\
...\\
\mu_p
\end{bmatrix}
\end{split}
\end{equation}

\(\underset{(p \times p)}{\Sigma}\) = Variance-Covariance Matrix

\(f(\vec{Y}) = \frac{1}{(2 \pi )^{\frac{P}{2}}
\sqrt{det(\Sigma)}}exp(-\frac{1}{2}(\vec{Y} - \vec{\mu})^T \Sigma^{-1}
(\vec{Y} - \vec{\mu}))\)

If \(Y_1, ..., Y_p\) are jointly normally distributed (i.e in the multivariate
normal distr.), then \(Y_k \sim N(\mu_k, \sigma^2_k)\) where \(k = [1, p]\)

Recall the Linear Regression equation \(Y_i \beta_0 + \beta_1 X_i + \epsilon_i\)
where \(\epsilon_i \sim N(0, \sigma^2)\).

\(\underset{(n \times 1)}{\vec{Y}} = \underset{(n \times 2)(2 \times 1)}{X
\vec{\beta}} + \vec{\epsilon}\) where \(\underset{(n \times 1)}{\vec{\epsilon}}
\sim N_n(\vec{0}, \sigma^2 I)\)

\(N_n\) is a dimensions of a multivariate normal

\(\vec{\beta} = \begin{bmatrix}
\beta_0\\
\beta_1
\end{bmatrix}\)

\(E(\vec{Y}) = X \vec{\beta}\)


<a id="orgf521527"></a>

### Least Squares Estimation

**Normal Equations from Week 2**

\begin{equation}
\begin{split}
n b_o + b_1 \Sigma x_i = \Sigma Y_i\\
b_0 \Sigma X_i + b_1 \Sigma X_i^2 = \Sigma X_i Y_i
\end{split}
\end{equation}

\(X^T X \vec{b} = X^T \vec{Y}\)

So?

**Least Squares Estimator**: \(\vec{b} = (X^T X)^{-1} X^T \vec{Y}\)

\(\underset{(n \times 1)}{\vec{\hat{Y}}} = \underset{(n \times 2)(2 \times
1)}{X \vec{b}} = (X^T X)^{-1} X^T \vec{Y}\)

1.  Hat Matrix

    \(H = (X^T X)^{-1} X^T\)
    
    The Hat Matrix is important for computing diagnostics for the model such as
    Cook's Distance.
    
    **Properties**
    
    -   symmetric (\(H^T = H\))
    -   Idempotent (\(HH = H\))

2.  Residuals

    \(E_i = Y_i - \hat{Y_i} \to \vec{Y} - \vec{\hat{Y}} = \vec{Y} - X \vec{b} =
    \vec{Y} - H \vec{Y} = (I - H) \vec{Y}\)
    
    \(\sigma^2(\vec{e}) = \sigma^2(I - H)\)
    
    This is estimated by: \(MSE (I - H)\)


<a id="org1f8b49e"></a>

# Session 6 - Sums of Squares and Multiple Linear Regression


<a id="org40f68c6"></a>

## Sum of Squares

\begin{equation}
\begin{split}
\underset{(1 \times n)(n \ times 1)}{\vec{Y}^T \vec{Y}} = \Sigma Y_i^2
\end{split}
\end{equation}

**Quadratic Form**: Contains squares of observations **and** their cross products.
 These are known as second-degree polynomials.

Quadratic forms scaled by \(\sigma^2\) allow us to treat the random variable Y as
an observation of \(\chi^2_{n - 1}\) distribution.

This is unlike \(\sigma^2 (A \vec{Y}) = A \sigma^2 (\vec{Y}) A^T\) since that is
squaring a matrix of **constants** whereas \(\vec{Y}^T \vec{Y}\) squares a matrix
of **random variables** i.e. Y


<a id="orgeec8fe5"></a>

### SSE

\begin{equation}
  \begin{split}
   SSE = & \Sigma e_i^2\\
       = & \vec{e}^T \vec{e}\\
       = & \vec{Y}^T (I - H) \vec{Y}
  \end{split}
\end{equation}


<a id="orgfda62a6"></a>

### SSTo

\begin{equation}
  \begin{split}
    SSTo = & \Sigma (Y_i - \bar{Y})^2\\
         = & \Sigma Y_i^2 - \frac{(\Sigma Y_i)^2}{n}\\
         = & \vec{Y}^T (I - \frac{1}{n} J) \vec{Y}
  \end{split}
\end{equation}


<a id="org68014fe"></a>

### SSR

\begin{equation}
  \begin{split}
    SSR = & \Sigma (\hat{Y_i} - \bar{Y})^2\\
        = & \vec{Y}^T (H - \frac{1}{n} J) \vec{Y}
  \end{split}
\end{equation}


<a id="orgc9dd64f"></a>

## Mean Estimates \(\sigma^2\)


<a id="orgebbf3a4"></a>

### Mean Responses

\(\hat{Y_h} = b_0 + b_1 X_h\)

so? we would like

\begin{equation}
\begin{split}
\underset{(1 \times 1)}{\hat{Y_h}} = \begin{bmatrix}
1 & X_h
\end{bmatrix}
\vec{b}
\end{split}
\end{equation}

Let \(\vec{X_h} = \begin{bmatrix}
1\\
X_h
\end{bmatrix}\)

Then, \(\hat{Y_h} = \vec{X_h}^T \vec{b}\)

This is an estimate of the mean response!


<a id="org0965fdd"></a>

## Variance of \(\hat{Y_h}\)

\begin{equation}
  \begin{split}
    \underset{(1 \times 1)}{Var(\hat{Y_h})} = & Var(\vec{X_h}^T \vec{b})\\
                                            = & \vec{X_h}^T Var(\vec{b}) \vec{X_h}\\
                                            = & \vec{X_h}^T \sigma^2(X^T X)^{-1} \vec{X_h}\\
                                            = & \underset{(1 \times 2)(2 \times 2)(2 \times 1)}{\sigma^2 X_h^T (X^T X)^{-1} \vec{X_h}}
  \end{split}
\end{equation}


<a id="orga98c238"></a>

## Multiple Regression Models

\(Y_i = \beta_0 + \beta_1 X_{i1} + ... + \beta_{p - 1} X_{i, p - 1} + \epsilon_i\)
where \(\epsilon_i \sim iid N(0, \sigma^2)\)

\(E(Y_i) = \beta_0 + \beta_1 X_{i1} + ... + \beta_{p - 1} X_{i, p - 1}\)

\(Y_i \sim indep N(E(Y_i), \sigma^2)\).

The parameters of this model are {&beta;<sub>0</sub>, &#x2026;, &beta;<sub>p</sub>}. Thus there are **p**
regression coefficients.


<a id="orge24de43"></a>

### Interpretation

Using the model, \(Y_i = \beta_0 + \beta_1 X_{i,1} + \beta_2 X_{i,2}\)

let's interpret the coefficients.

\(\beta_0\): The mean response of Y when \(X_1 = 0, X_2 = 0\)

\(\beta_1\): For a fixed value of \(X_2\), the associated increase in mean response
in Y is \(\beta_1\) for every 1 unit increase in \(X_1\). **This is known as a
partial effect**

\(\beta_2\): For a fixed value of \(X_1\), the associated increase in mean response
in Y is \(\beta_2\) for every 1 unit increase in \(X_2\).

\(\beta_k\): Associated change in mean response of Y for every 1 unit increase in
\(X_k\), given all other predictors are held constant.


<a id="org1812ba6"></a>

### Aside: Multi-Collinearity

**Multicollinearity** occurs when two or more predictors are highly correlated.

-   Standard Errors blow up which makes test statistic small, which makes p-values
    high. This affects the ability for us to make **inferences**
-   Multicollinearity is acceptable when using models for **prediction** but not
    when using them for **inference**.


<a id="org36a3107"></a>

### Matrix Notation

\begin{equation}
  \begin{split}
    \underset{(n \times 1)}{\vec{Y}} = & \underset{(n \times p)(p \times 1)}{X \vec{\beta}} + \underset{(n \times 1)}{\vec{\epsilon}}\\
    \underset{(n \times n)}{Var(\vec{\epsilon})} = & \sigma^2 I
  \end{split}
\end{equation}

1.  Fitted Values

    \(\hat{Y_i} = b_0 + b_1 X_{i,1} + ... + b_{p - 1} X_{i, p - 1}\)
    
    **Residuals**: \(e_i = Y_i - \hat{Y_i}\)

2.  Least Squares Estimators

    \(\underset{(p \times 1)}{\vec{b}} = \underset{(p \times n)(n \times p)}{(X^T
    X)^}{-1}} \underset{(p \times n)(n \times 1)}{X^T \vec{Y}}\)


<a id="orgf0ffece"></a>

### ANOVA Table

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Source</th>
<th scope="col" class="org-left">SS</th>
<th scope="col" class="org-left">DF</th>
<th scope="col" class="org-left">MS</th>
<th scope="col" class="org-left">F</th>
<th scope="col" class="org-left">p-value</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Regression</td>
<td class="org-left">SSR = \(\Sigma (\hat{Y_i} - \bar{Y})^2\)</td>
<td class="org-left">p - 1</td>
<td class="org-left">MSR = \frac{SSR}{p - 1}</td>
<td class="org-left">\(F^* = \frac{MSR}{MSE}\)</td>
<td class="org-left">\(P(F_{p-1, n-p} \geq F^*)\)</td>
</tr>


<tr>
<td class="org-left">Error</td>
<td class="org-left">SSE = \(\Sigma (Y_i - \hat{Y_i})^2\)</td>
<td class="org-left">n - p</td>
<td class="org-left">MSE = \frac{SSE}{n - p}</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Total</td>
<td class="org-left">SSto = \(\Sigma (Y_i - \bar{Y})^2\)</td>
<td class="org-left">n - 1</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>


<a id="org3b3489d"></a>

### Omnibus F-Test for Regression Relation

\begin{equation}
  \begin{split}
    H_0: \beta_1 = \beta_2 = ... = \beta_p = 0\\
    H_A: \text{ at least one } \beta_k \neq 0
  \end{split}
\end{equation}

Test statistic: \(F^* = \frac{MSR}{MSE}\).
If \(H_0\) is true, \(F^* \sim F_{p - 1, n - p}\)


<a id="org7a723d6"></a>

### Coefficient of Multiple Determination

\(R^2 = 1 - \frac{SSE}{SSTo}\)

The issue with \(R^2\) is that it increases with the number of predictors
**irrespective** of the predictor improving the model.

\(R_{adj}^2 = 1 - \frac{\frac{SSE}{n - p}}{\frac{SSTo}{n - 1}}\)


<a id="orgdcb482a"></a>

### Coefficient of Multiple Correlation

\(R = \sqrt{R^2}\)


<a id="org862633a"></a>

### Inferences in \(\beta_k\)

\begin{equation}
  \begin{split}
    H_0: \beta_k = 0\\
    H_A: \beta_k \neq 0
  \end{split}
\end{equation}

**Test Statistic**: \(t^* = \frac{b_k}{SE_{bk}}\)

If \(H_0\) is true, then \(t^* \sim t_{n - p}\)

p-value = \(2 P(t_{n - p} \geq |t|)\)

    2 * (1 - pt(abs(t.star), n - p))

\(100(1 - \alpha)%\) C.I. for \(\beta_k\): \(b_k \pm t_{1 - \frac{\alpha}{2}, n - p} SE_{bk}\)


<a id="org979fa60"></a>

# Session 7 - Multiple Regression & Qualitative\\/Quantitative Predictors


<a id="orgb7adc46"></a>

## Multiple Regression


<a id="orgcdc104d"></a>

### Extra Sums of Squares

**Def**: The marginal reduction in SSE when one or several predictors are added to
the regression model, **given** other predictors are already in the model.

\(SSR(X_2 | X_1) = & SSE(X_1) - SSE(X_1, X_2)\\
  SSR(X_2 | X_1) = & SSR(X_1, X_2) - SSR(X_1)\)

These are equivalent because any reduction in SSE implies an increase in SSR per
the ANOVA definition: \(SSTo = SSR + SSE\)

1.  Multiple Predictors

    \(SSR(X_3 | X_1, X_2) = & SSE(X_1, X_2) - SSE(X_1, X_2, X_3)\\
    SSR(X_3 | X_1, X_2) = & SSR(X_1, X_2, X_3) - SSR(X_1, X_2)\)
    
    \(SSR(X_1, X_2) = SSR(X_2) + SSR(X_1 | X_2)\)
    
    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="org-left" />
    
    <col  class="org-left" />
    
    <col  class="org-right" />
    
    <col  class="org-left" />
    </colgroup>
    <thead>
    <tr>
    <th scope="col" class="org-left">Source</th>
    <th scope="col" class="org-left">SS</th>
    <th scope="col" class="org-right">df</th>
    <th scope="col" class="org-left">MSE</th>
    </tr>
    </thead>
    
    <tbody>
    <tr>
    <td class="org-left">Regression</td>
    <td class="org-left">\(SSR(X_1, X_2, X_3)\)</td>
    <td class="org-right">3</td>
    <td class="org-left">\(MSR(X_1, X_2, X_3)\)</td>
    </tr>
    
    
    <tr>
    <td class="org-left">\(X_1\)</td>
    <td class="org-left">\(SSR(X_1)\)</td>
    <td class="org-right">1</td>
    <td class="org-left">\(MSR(X_1)\)</td>
    </tr>
    
    
    <tr>
    <td class="org-left">\(X_2 \vert X_1\)</td>
    <td class="org-left">\(SSR(X_2 \vert X_1)\)</td>
    <td class="org-right">1</td>
    <td class="org-left">\(MSR(X_2 \vert X_3)\)</td>
    </tr>
    
    
    <tr>
    <td class="org-left">\(X_3 \vert X_1, X_2\)</td>
    <td class="org-left">\(SSR(X_3 \vert X_1, X_2)\)</td>
    <td class="org-right">1</td>
    <td class="org-left">\(MSR(X_3 \vert X_1, X_2\))$</td>
    </tr>
    
    
    <tr>
    <td class="org-left">Error</td>
    <td class="org-left">\(SSE(X_1, X_2, X_3)\)</td>
    <td class="org-right">n - 4</td>
    <td class="org-left">\(MSE(X_1, X_2, X_3)\)</td>
    </tr>
    
    
    <tr>
    <td class="org-left">Total</td>
    <td class="org-left">SSTo</td>
    <td class="org-right">n - 1</td>
    <td class="org-left">&#xa0;</td>
    </tr>
    </tbody>
    </table>

2.  Hypothesis Test - \(\beta_k = 0\)

    \(H_0: \mu_k = 0\\
    H_A: \mu_k \neq 0\)
    
    This is the \(\mu_k X_k\) dropped from the model.
    
    **Test Statistic**: \(t^* = \frac{b_k}{SE_{bk}}\) \(df = n - p\)
    
    1.  Full model
    
        \(Y_i = \mu_0 + \mu_1 X_1 + ... + \mu_{p - 1} X_{i, p-1} + \epsilon_i\)
        
        "p - 1" predictor variables
        
        \(SSE(F) = SSE(X, ..., X_{p - 1})\)
    
    2.  Reduced Model
    
        \(Y_i = \mu_0 + \mu_1 X_1 + ... + \mu_{p - 2} X_{i, p - 2} + \epsilon_i\)
        
        "p - 2" predictor variables
        
        \(SSE(R) = SSR(X, ..., X_{k - 1}, X_{p - 1})\)
        
        \(F^* = SSE(R) - SSE(F) = \frac{df_R - df_F}{\frac{SSE(F)}{df_F}} = \frac{
        \frac{SSE(X_1, ..., X_{k - 1}, X_k, ..., X_{p - 1}) - SSE(X, ..., X_{p -
        1})}{n - (p - 1) - (n - p)}}{\frac{SSE(X, ..., X_{p - 1})}{n - p}}\)

3.  Hypothesis Test - \(\beta_0 = ... = \beta_k = 0\)

    1.  Reduced Model
    
        \(Y_i = \mu_0 + \mu_1 X_{i1} + ... + \mu_{k - 1} X_{i,k - 1} + \mu_k X_{ik} + ... + \mu_{p - 1} X_{i, p - 1} + \epsilon_i\)
        
        "p - g - 1" predictors **OR** "p - g" regression coefficients
        
        \(F^* = \frac{\frac{SSE(X_1, ..., X_{k - 1}, X_k, ..., X_{p - 1}) - SSE(X, ..., X_{p -
        1})}{n - (p - g) - (n - p)}}{\frac{SSE(X, ..., X_{p - 1})}{n - p}} = \frac{SSR(X_k, ..., X_{k + (g - 1)} |
        X_k, ..., X_{k + g}, ..., X_{p - 1})}{MSE(X_1, ..., X_{p - 1})}\)
        If \(H_0\) is true, \(F^* \sim F_{g, n - p}\)

4.  \(R^2\)

    \(R^2\): Coefficient of multiple determination
    
    -   proportion of variation in Y explained by the regression of Y on \(X_1, ...,
          X_{p - 1}\)
    
    <span class="underline">Ex</span>
    
    \(Y_i = \mu_0 + \mu_1 X_{i,1} + \mu_2 X_{i,2}\)
    
    \(SSE(X_2)\): variation when only \(X_2\) is in the model.
    
    \(SSE(X_1, X_2)\): variation when both \(X_1,X_2\) are in the model.
    
    Marginal reduction in variation when X<sub>1</sub> is added to the model?
    
    \(\frac{SSE(X_2) - SSE(X_1, X_2)}{SSE(X_2)}\)
    
    \(R_{Y_1/Y_2}^2 = \frac{SSR(X_1 | X_2)}{SSE(X_2)}\)
    
    \(R_{Y_2/Y_1}^2 = \frac{SSR(X_2 | X_1)}{SSE(X_1)}\)
    
    3 predictors
    
    \(R_{Y3|2,1}^2 = \frac{SSR(X_3 | X_1, X_2)}{SSE(X_1, X_2)}\)
    
    Recipe for correlation coefficient:
    
    1.  Take sqrt of partial \(R^2\)
    2.  Sign of partial correlation = sign of correlation corresponding coefficient


<a id="org4caf32a"></a>

## Multi-collinearity

Predictors that are highly correlated with each other. **10 N values per predictor**


<a id="orgaccaf69"></a>

### Effects

1.  There is no unique sum of squares that can be assigned to the predictor
    variable
2.  May inflate standard error of \(b_k\) least square error.

It does not greatly impact the value of predictions.

\({ETA}^2\) tells \(R^2\) given the previously given variable \(R^2\)


<a id="orge0fb7fb"></a>

## Polynomial Regression Models

-   true curvilinear response
-   true curvilinear response is unknown but a polynomial function provides a good
    approximation to the true function.

One prediction variable **and** second order:

\(Y_i = \mu_0 + \mu_1 X + \mu_2 X^2 + \epsilon_i\) where \(X_i = x_i - \bar{x}\)

\(E(Y) = \mu_0 + \mu_1 X_1 + \mu_2 X^2\)

Two parameters **and** second order:

\(x_{i,1} = x_{i,1} - \bar{x_1}\)

\(X_{i,2} = x_{i,2} - \bar{x_2}\)

\(Y_i = \beta_0 \beta_1 X_{i,1} + \beta_2 X_{i,2} + \beta_3 X_{i,1}^2 + \beta_4
X_{i,2}^2 + \beta_5 X_{i,1} X_{i,2} + \epsilon_i\)

<span class="underline">Strategy?</span> Fit higher order models and compare to reduced models.

    summary(model)

\(\hat{Y} =  b_0 + b_1 x + b_2 x^2\)
\(\hat{Y} =  b_0' + b_1' x + b_2' x^2\)

\(b_0' = b_0 - b_1 \bar{x} - b_2 \bar{x}^2\)

\(b_1' = b_1 - 2 b_2 \bar{x}\)

\(b_2' = b_2\)

Why do this? Solving a regression model with a non-linear \(E(Y_i)\)


<a id="org42b0744"></a>

# Session 8 - Interaction Models & Model Selection


<a id="orgee2a372"></a>

## Interaction Regression Models

-   p: # of regression coefficients. i.e. parameters
-   p - 1: predictor variables


<a id="org28d0157"></a>

### Additive Effects

\begin{equation}
\begin{split}
E(Y) = \sum_{i = 1}^{p - 1} f_K(x_k)
\end{split}
\end{equation}

**but** \(E(Y) = \beta_0 + \beta_1 X_1 + \beta_2 X_2 \ \beta_3 X_1 X_2\) is **not**
 additive since \(X_1 X_2\) is an interaction term

Consider the following:

\(Y_i = \beta_0 + \beta_1 X_1 + \beta_2 X_2 \ \beta_3 X_1 X_2 + \epsilon_i\) where
\(\epsilon_i \sim iid N(0, \sigma^2)\)

A one-unit **increase** in \(X_2\) for a fixed value of \(X_1\), results in an
associated change of \(\beta_1 + \beta_3 X_1\) units in mean response Y.

-   \(\beta_3 = 0\) => additive model
-   \(\beta_3 > 0\) => reinforcement or synergistic interaction\*
-   \(\beta_3 < 0\) => interference or antagonistic interaction\*

\*if \(\beta_1\) and \(\beta_2\) are negative, these terms flip

parallel lines indicate **additive** terms, otherwise <span class="underline">interactive</span>

**Aside**

> To avoid multicollinearity between predictors, center variables!
>  \(X_{ik} = X_{ik} - \bar{X_k}\)
> 
> Does Standardizing also help reduce multicollinearity? Yes, but makes
> interpretation more difficult. This is done in PCA and as I've seen,
> interpreting PCA can be hairy or a best guess.

-   Try to identify possible interactions ahead of time prior to fitting the
    model.
-   When looking at removing **one** term, the \(t\) statistic is sufficient to rule
    out a parameter.


<a id="orgf20aaec"></a>

### Qualitative Predictors

Qualitative Predictor with two classes. i.e. two values
This is sometimes called: Indicators, Binary, dummy variables

For representing \(C\) classes, use \(C - 1\) indicator variables.

<span class="underline">Example</span>

Let C = 4
\(C =\begin{bmatrix}
A\\
B\\
C\\
D
\end{bmatrix}\)

\begin{equation}
\begin{split}
Y_i = & \beta_0 + \beta_1 X_1 + \beta_2 X_2 \ \beta_3 X_3 + \beta_4 X_4 + \epsilon_i \text{ where }\\
X_2 = & \begin{cases}
1, &  A\\
0, & else
\end{cases}\\
X_3 = & \begin{cases}
1, &  B\\
0, & else
\end{cases}\\
X_4 = & \begin{cases}
1, &  C\\
0, & else
\end{cases}
\end{split}
\end{equation}

if \(X_2 = X_3 = X_4 = 0\), indicates effect of \(C = D\) on mean \(Y_i\)

\begin{equation}
\begin{split}
A: E(Y) = & (\beta_0 + \beta_2) + \beta_1 X_i\\
B: E(Y) = & (\beta_0 + \beta_3) + \beta_1 X_i\\
C: E(Y) = & (\beta_0 + \beta_4) + \beta_1 X_i\\
D: E(Y) = & (\beta_0) + \beta_1 X_i
\end{split}
\end{equation}

D is considered the **baseline category**

1 Qualitative variable and 1 Quantitative variable in the same model is known as
**ancova**: Analysis of Covariance. ANCOVA assumes that each group has the same slope.

<span class="underline">Interpret \(\beta_0\)</span>: The diff in mean response of \(Y\) between \(A\) and \(D\)
group for a given value of \(X_1\)

**Estimate \(\beta_3 - \beta_4\)**

1.  \(b_3 - b_4\)
2.  \(Var(b_3 - b_4) = var(b_3) + var(b_4) - 2 cov(b_3, b_4)\)

If doing time series, one can use indicator variables to model time periods


<a id="org2ff8ed6"></a>

## Model and Variable Selection


<a id="org9bc084b"></a>

### Criterion for Model Selection

p: # of parameters (regression coefficients)

1.  \(R^2_p\) or \(SSE_p\) criterion. Both indicate the same thing.
    
    \(R_p^2 = 1 -\frac{SSE_p}{SSTo}\)
    
    **Look for**
    
    -   *High* \(R_p^2\)
    -   *Small* \(SSE_p\)

2.  \(R_{a,p}^2\) or \(MSE_p\) criterion
    
    \(R_p^2 = 1 -\frac{\frac{SSE_p}{n- p}}{\frac{SSTo}{n - 1}} = 1 -
       \frac{MSE_p}{\frac{SSTo}{n - 1}}\)
    
    **Look For**:
    
    -   *High* \(R_{a,p}^2\)
    -   *Small* \(MSE_p\)

3.  Mallows' \(C_p\) Criterion
    
    \(C_p = \frac{SSE_p}{MSE(X_1, ..., X_{p - 1})} - (n - 2p)\)
    
    \(MSE(X_1, ..., X_{p - 1})\): MSE for the model with **all** potential predictors
    of interest.
    
    For largest possible value of \(P\), \(C_p = p\)
    
    <span class="underline">proof</span>

\begin{equation}
\begin{split}
MSE = & \frac{SSE}{n - p}\\
\frac{SSE_p}{\frac{SSE_p}{n - p}} = & n - p - (n - 2p) =  p
\end{split}
\end{equation}

**Look for**

-   *Small* \(C_p\) <span class="underline">or</span> \(C_P \leq p\). This means the model has a small amount of
    bias.

Recall \(MSE(Y) = Bias^2(Y) + Var(Y)\)

1.  \(AIC_p\) or \(SBC_p\) Criterion
    
    -   \(AIC_p\): Akaike's Information Criterion - \(n ln(SSE_p) - n ln(n) + 2p\)
    -   \(SBC_p\): Schwartz' Bayesian Information Criterion - \(n ln(SSE_p) - n
             ln(n) + p ln(n)\)
    
    **Look for**
    
    -   *Small* \(SSE_p\)
    -   *Small* \(AIC_p\) and/or \(SBC_p\)

2.  \(PRESS_p\) Criterion
    
    Prediction Sum of Squares
    
    \(PRESS_P = \sum_{1}^{n} (Y_i - \hat{Y_{i (i)}})^2\)
    
    **\(\hat{Y_{i(i)}}\)**
    
    1.  Ignore the ith case
    2.  Fit model on remaining \(n - 1\) cases
    3.  Find Fitted value based on deleted ith case
    
    This is **not** the same as bootstrapping, mostly because there is no
    resampling oging on.
    
        leaps::regsubsets(formula, data, method="exhaustive", nbest=30)
    
         #+NAME: fortify_leaps
         fortify.regsubsets <- function(model, data, ...){
           require(plyr)
           stopifnot(model$intercept)
           models <- summary(model)$which
           rownames(models) <- NULL
           model_stats <- as.data.frame(summary(model)[c("bic","cp","rss","rsq","adjr2")])
           dfs <- lapply(coef(model, 1:nrow(models)), function(x) as.data.frame(t(x)))
           model_coefs <- plyr::rbind.fill(dfs)
           model_coefs[is.na(model_coefs)] <- 0
           model_stats <- cbind(model_stats, model_coefs)
           # terms_short <- abbreviate(colnames(models))
           terms_short <- colnames(models)
           model_stats$model_words <- aaply(models, 1, function(row) paste(terms_short[row], collapse = "+"))
           model_stats$size <- rowSums(summary(model)$which)
           model_stats
         }
        
         get_model_coefs <- function(model){
           models <- summary(model)$which
           dfs <- lapply(coef(model, 1:nrow(models)), function(x) as.data.frame(t(x)))
           model_coefs <- plyr::rbind.fill(dfs)
           model_coefs[is.na(model_coefs)] <- 0
           model_coefs
        }
