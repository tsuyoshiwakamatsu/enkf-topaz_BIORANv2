# TOPAZ EnKF with BGC assimilation

### main update

Following updates are for making TOPAZ EnKF flexible for hycom configuration options:

- hycom configuration files: ```regional.grid.(a,b)```, ```regional.depth.(a,b)``` and ```grid.info```, are read through a new module:
```
get_mod_cnfg
```
instead of being read from ```depth*.uf```.

#### notes:

- ```depth``` read from ```regional.depth.(a,b)``` is used for making land mask in ```Prep_Routines``` without using ```meanssh.uf```
- configuration specific ```meanssh.uf``` and ```re_sla.nc``` are still required for SLA data prepobs.

### TODO:

- read ```meanssh.nc``` only for SLA assimilation
