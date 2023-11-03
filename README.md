Code package for Hauzenberger, N., F. Huber, & G. Koop (2023). Macroeconomic forecasting using BVARs. Chapter for *Handbook of Macroeconomic Forecasting*, edited by Mike Clements and Ana Galvão.

**Publication ([draft chapter](https://www.dropbox.com/scl/fi/cry8xuxkwwdtc3matz8g1/HHK_bookchp.pdf?rlkey=45ysy3b2hpqykkxormms9bipe&dl=0)).** 

### Data. 
For the forecast exercise, we use the popular FRED-QD dataset provided by the *Federal Reserve Bank of St. Louis* (https://research.stlouisfed.org/econ/mccracken/fred-databases/). We provide the raw-data as a .rda file (fred_data/fred_QD.rda) with the 30 columns of the Xraw.stat object referring to the different variables. Our quarterly sample runs from $1965$Q$1$ to $2019$Q$4$. We deliberately exclude the Covid-19 period and focus exclusively on pre-pandemic data. We transform the data to stationarity, according to the suggestions of McCracken and Ng (2020). Table 1 in Sub-section 4.1 of the bookchapter  shows the set of variables included for the different model sizes. For each model type we specify an estimation grid over the full hold-out sample and the information set. In terms of model specifications, we consider four conjugate and four non-conjugate VAR priors. Below we provide details on how we estimate these different models. We have three main estimation/forecasting files: one for conjugate BVARs (!fcst_conjVAR.R), one for conjugate BVARs with sub-space shrinkage (!fcst_subVAR.R), and one for non-conjugate BVARs (!fcst_nconjVAR.R).

