# MT dyanamics simulation
This is a simulation of microtubule dynamics simply assuming growth rate, shrinkage rate, catastrophe frequency and rescue frequency

For simulation, assign a parameter set to the variable `param` in Microtubule_dynamic_simulation.Rmd.
```{r}
param <- tibble(
    group_name = c("Control", "Kinesin-13 KO"),
    mean_gr = c(0.147, 0.093), # mean growth rate
    sd_gr =  c(0.029, 0.006), # SD shrinkage rate
    mean_sr = c(0.245, 0.429), # mean shrinkage rate
    sd_sr = c(0.059, 0.107), # SD shrinkage rate
    cat_freq = c(0.0093, 0.0022), # Catastrophe frequency
    res_freq = c(0.014, 0.025), # Rescue frequency
    time = rep(240, length(group_name)), # Time duration 240 s, 4 min
  )
  ```
