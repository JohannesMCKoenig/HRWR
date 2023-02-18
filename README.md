# HRWR
Replication files for:

Hours Risk and Wage Risk: Repercussions over the Life-Cycle 


Robin Jessen (rjessen@rwi-essen.de)
Johannes König (jkoenig@diw.de)

The data set used for this paper is the PSID, which restricts free sharing of the data. Researchers can obtain the data here: https://psidonline.isr.umich.edu/


This document explains where one can find the code that generates
each table, figure and calculation in the text in the codebase
in order of appearance in the paper.

Overall, the code can be understood in the following way:

1. "estimations" contains the Stata based code for preparing the dataset
   and estimating the IV model to obtain the Frisch elasticity of labor supply.
   Paths have to be adjusted in "doall".
   The code also prepares the wage and hours residuals used in the fitting of the structural model.

2. "boot" contains the estimation(s) of the model(s) using Wolfram Mathematica.
    The models can generally be started from the "Run" files. 
    Paths have to be adjusted in the "Run" and "set_paths" fils.
    Subfolder "main" contains the estimation for the main and the additional samples.
    "altsamps" contains the estimation for alternative samples.
    "altmods" contains the estimation for alternative model specifications.
    Finally, "appendix" contains estimation files for models shown in the appendix.

3. "modelbased_calculations" contains various Mathematica and Stata files to calculate
    the earnings growth variance and risk decomposition as well as other calculations
    presented in the text. 



***Tables***

Table 1: 
		~\estimations\estimations\estimations.do Line 76

Table 2 + 3: 		
  		~\boot\main\Run.nb

Table 4: 
		~\estimations\estimations\estimations.do  Line 158  
		~\modelbased_calculations\DecompOfWageandHoursGrowthVariance.nb

Table 5:
		~\modelbased_calculations\DecompOfEarningsGrowthVarAndRisk.nb

Table 6:
		~\modelbased_calculations\DecompOfEarningsGrowthVarAndRisk.nb

Table 7: 		
  		~\boot\altsamps\Run.nb

Table 8: 		
  		~\boot\altmods\Run.nb

Table 9: 		
  		~\modelbased_calculations\EffectShockLifetimeEarningsAndConsumption.do

Table A1:
		 ~\estimations\estimations\estimations.do  Line 186

Table A2: 
		 ~\estimations\estimations\doall.do Line 187

Table A3: 
		 ~\estimations\estimations\estimations.do  Line 102
		 ~\boot\appendix\frisch\Run.nb

Table A4: 
	Col 1: 
		 ~\boot\appendix\run_nopersist\Run.nb
	Col 2: 
		 ~\boot\appendix\cohorts\Run.nb

Table A5: 	
		~\modelbased_calculations\DecompOfEarningsGrowthVarAndRisk.nb

***Figures***

Figure 1:
		 ~\estimations\estimations\estimations.do  Line 168 

Figure 4:
		 ~\estimations\estimations\estimations.do  Line 358 
	       ~\boot\main\Run_momfit.nb


Figure A.1:
		 ~\estimations\estimations\estimations.do  Line 358 
		 ~\boot\appendix\cohorts\Run_momfit.nb

Figure C.2:
		 ~\estimations\estimations\estimations.do  Line 168 

Figure D.3:
		~\estimations\estimations\estimations.do  Line 80 

***Calculations in Text***

Footnote 7:
		~\modelbased_calculations\PermHshocksDueToFemaleWShocks.nb

Page 28: 
		~\modelbased_calculations\CalculationOfShockImpactOnEarnings.nb

Pages 28-29:
		~\modelbased_calculations\EffectShockLifetimeEarningsAndConsumption.do
