# epp 0.3

- Implement ANC routine testing (ANC-RT) likelihood in EPP 2017 (Spectrum 5.52)

# epp 0.3.1

- Updates to IMIS optimization step:
 - Do random sample as well in each iteration
 - Reduce numerical integration stepsize and try again if BFGS encounters non-finite difference error
 - Use last value from center_all to initialise optimization if no positive samples remain

# epp 0.3.2

- ~~IMIS offsets likelihood by maximum log-likelihood to avoid underflow.~~  Rolled this back because it introduced a pernicious little bug in mixture weights when offset changes numerical underflow. Should be re-implemented more carefully later.
- Added option to likelihood() to return log values.

# epp 0.3.3

- Only read ANC-RT data if used in EPP fit
