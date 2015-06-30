# Temporal-RI
This is an implementation of Bertrand et al. (2003) temporal randomization inference in R. Read pages 20 through 22 in here: http://www.nber.org/papers/w8841.pdf 
Bertrand et al. (2003) suggest a new approach in studying the causality in a field experimental setting. Let's say we have a model in the form: y_it = a_i + m_t + bT_it + e_it
where i stands for the entity under study (individual, state, ...), t is the time of observation, a_i is the individual-specific effects, m_t is the time-fixed effects, b is the treatment effect to be estimated, T_it is the treatment and 
e_it is the error term. Using OLS or other specification, b can be estimated.   
To study the causal relationship, one can simulate the time of treatment (and the treated individuals) and estimate b for multiple times over random;y treated individuals.
If the number of simulation is large enough, a distribution for b can be obtained. The last step is to check where the actual b falls in the simulated b distribution. If the actual b is statistically outside the distribution of simulated b, we can coclude that the treatment effect was indeed significant. 
To use this script, you need to prepare your data in both long and wide formats. 
