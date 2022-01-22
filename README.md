# FractionalDerivative

We do the fractional derivative from the Bovespa Series.

More spefically we use the values from ABEV3 from 1994 to 2020. 

- The goal of fractional differentiation is to find the fraction d, which we call the minimum differentiation order: it is the minimum number needed to achieve stationarity while maintaining the maximum amount of memory in our data.
- The calculated weight is a feature to give importance to the most recent values. The current timestamp can be expressed as the sum of all previous values with a weight assigned to each value. 
- By controlling the weight limit, we actually control the length of memory rather than the amount of memory (the first few points have more weight, therefore more memory).

To calculate the minimum coefficient d, we will use the Augmented Dickey-Fuller test, which is a type of statistical test called the unit root test. The null hypothesis of the test is that the time series can be represented by a unit root, which is not stationary (has some time-dependent structure).

O teste pode ser interpretado pelo  **p-value**. Um valor p abaixo de um limite 5% definido está sugerindo sugere que rejeitamos a hipótese nula (estacionário).

![Result](https://raw.githubusercontent.com/hojentropia/FractionalDerivative/main/graph.png)
