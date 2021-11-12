 * [1 Pediatric Qualification Package: CYP3A4 Ontogeny](#1-pediatric-qualification-package-cyp3a4-ontogeny)
   * [1.1 Translation of Adult PBPK to Children](#11-translation-of-adult-pbpk-to-children)
   * [1.2 Anthropometric and Physiological Information ](#12-anthropometric-and-physiological-information-)
   * [1.3 Qualification of **CYP3A4 enzyme ontogeny**](#13-qualification-of-cyp3a4-enzyme-ontogeny)
   * [1.4 Evaluation of Pediatric translation](#14-evaluation-of-pediatric-translation)
     * [1.4.1 Sufentanil model](#141-sufentanil-model)
       * [1.4.1.1 Concentration-Time Profiles](#1411-concentration-time-profiles)
     * [1.4.2 Alfentanil model](#142-alfentanil-model)
       * [1.4.2.1 Concentration-Time Profiles](#1421-concentration-time-profiles)




# 1 Pediatric Qualification Package: CYP3A4 Ontogeny





| Version                         | x.x-OSPy.y                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP3A4_Ontogeny/releases/tag/vx.x |
| OSP Version                     | y.y                                                          |
| Qualification Framework Version | z.z                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports





The presented qualification report evaluates the predictive performance of the OSP suite to predict cytochrome P450 3A4 (CYP3A4)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for dynamic pediatric translation in organs expressing CYP3A4. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age-related CYP3A4-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented (https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP3A4_Ontogeny). 


## 1.1 Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[Maharaj 2013](#3-references)] 

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature, covering available dosing ranges for e.g. intravenous as well as oral administration, to capture both systemic clearance as well gut-wall metabolic clearance processes. For orally administered drugs, the same formulations that are used in children should ideally be included in the model for adults. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed area under the plasma concentration (AUC)-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children as in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity, intestinal permeability, solubility) were kept unchanged.

## 1.2 Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published [[Edginton 2006](#3-references)]. The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The  applied ontogeny and variability of plasma proteins and active processes that are integrated into PK-Sim® for translation to children are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[Ontogeny Database](#3-references)] or otherwise referenced for the specific process.

## 1.3 Qualification of **CYP3A4 enzyme ontogeny**

To qualify the OSP suite for the pediatric translation of the pharmacokinetics of new drugs that are metabolized by CYP3A4, the following set of probe substances was included:

- Alfentanil [[Alfentanil-Model](#3-references)]

- Sufentanil [[Sufentanil-Model](#3-references)]

The adult PBPK model reports and the corresponding PK-Sim project files are filed at: https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/






## 1.4 Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:

Eq. 1: GMFE=10^((S|log10(pred PK parameter/obs PK parameter)|)/n)

with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  



Table 1: Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Study ID           |Age [year(s)] |Body Weight [kg] |Observed AUC [µmol*min/l] |Predicted AUC [µmol*min/l] |Pred/Obs AUC Ratio |
|:------------------|:-------------|:----------------|:-------------------------|:--------------------------|:------------------|
|Davis 1987         |1.29          |8.90             |2.14                      |1.16                       |0.54               |
|Davis 1987         |0.43          |5.30             |1.41                      |1.45                       |1.03               |
|Guay 1991          |2.08          |12.10            |0.28                      |0.17                       |0.60               |
|Guay 1991          |2.58          |16.00            |0.12                      |0.10                       |0.86               |
|Guay 1991          |2.67          |11.30            |0.23                      |0.26                       |1.13               |
|Guay 1991          |3.25          |16.00            |0.21                      |0.22                       |1.05               |
|Guay 1991          |3.83          |14.20            |0.17                      |0.14                       |0.84               |
|Guay 1991          |4.58          |15.00            |0.17                      |0.11                       |0.66               |
|Guay 1991          |4.58          |19.00            |0.35                      |0.22                       |0.63               |
|Guay 1991          |4.83          |17.50            |0.18                      |0.23                       |1.25               |
|Guay 1991          |5.25          |18.50            |0.11                      |0.12                       |1.04               |
|Guay 1991          |5.25          |19.65            |0.22                      |0.23                       |1.04               |
|Guay 1991          |5.33          |24.00            |0.35                      |0.29                       |0.83               |
|Guay 1991          |5.33          |24.00            |0.20                      |0.16                       |0.84               |
|Guay 1991          |5.75          |14.50            |0.39                      |0.20                       |0.50               |
|Guay 1991          |5.92          |28.20            |0.33                      |0.24                       |0.73               |
|Guay 1991          |5.92          |25.00            |0.15                      |0.12                       |0.84               |
|Guay 1991          |6.92          |29.60            |0.16                      |0.16                       |1.01               |
|Guay 1991          |7.50          |23.50            |0.09                      |0.07                       |0.77               |
|Guay 1991          |7.50          |15.20            |0.19                      |0.19                       |0.99               |
|Guay 1991          |8.75          |22.60            |0.15                      |0.14                       |0.93               |
|den Hollander 1992 |0.92          |6.50             |50.66                     |50.01                      |0.99               |
|den Hollander 1992 |0.83          |6.40             |33.61                     |50.75                      |1.51               |
|den Hollander 1992 |0.99          |8.50             |47.54                     |54.22                      |1.14               |
|den Hollander 1992 |0.30          |5.10             |44.42                     |67.61                      |1.52               |
|den Hollander 1992 |0.92          |6.15             |38.17                     |42.72                      |1.12               |
|den Hollander 1992 |1.30          |10.40            |58.34                     |50.97                      |0.87               |
|den Hollander 1992 |9.00          |25.60            |27.13                     |46.58                      |1.72               |
|den Hollander 1992 |3.50          |14.40            |44.66                     |45.32                      |1.01               |
|den Hollander 1992 |5.50          |19.50            |49.70                     |45.40                      |0.91               |
|den Hollander 1992 |3.50          |18.50            |54.50                     |49.18                      |0.90               |
|Meistelman 1987    |4.70          |20.00            |14.12                     |9.82                       |0.70               |
|Meistelman 1987    |5.50          |20.00            |8.14                      |9.10                       |1.12               |
|Meistelman 1987    |7.70          |23.00            |5.79                      |9.06                       |1.57               |
|Meistelman 1987    |4.50          |14.00            |10.44                     |7.81                       |0.75               |
|Meistelman 1987    |4.80          |24.00            |12.98                     |11.61                      |0.89               |
|Meistelman 1987    |4.50          |20.00            |10.00                     |10.07                      |1.01               |
|Meistelman 1987    |6.20          |23.00            |10.91                     |9.86                       |0.90               |
|Meistelman 1987    |4.90          |22.00            |17.78                     |10.51                      |0.59               |


Table 2: GMFE for Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Parameter |GMFE |
|:---------|:----|
|AUC       |1.25 |


Figure 1: Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


![](002_section_3/3-pk-ratio-plot-AUC.png)


Table 3: Measure of Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|                       | Number|Ratio |
|:----------------------|------:|:-----|
|Points Total           |     39|NA    |
|Points within 1.5-fold |     29|0.74  |
|Points within 2-fold   |     38|0.97  |





### 1.4.1 Sufentanil model

Sufentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Davis PJ, Cook DR, Stiller RL, Davin-Robinson KA. Pharmacodynamics and pharmacokinetics of high-dose sufentanil in infants and children undergoing cardiac surgery. Anesth Analg. 1987 Mar;66(3):203-8.[[Davis 1987](#3-references)]
- Guay J, Gaudreault P, Tang A, Goulet B, Varin F. Pharmacokinetics of sufentanil in normal children. Can J Anaesth. 1992 Jan;39(1):14-20.[[Guay 1992](#3-references)]

The pediatric PBPK model predicted the clearance values of sufentanil observed in pediatric studies reasonably across all available age groups, ranging from 5 months to 8.75 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that most predictions in children were within 2-fold error of observed values.



Table 4: Overall predictivity of the sufentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of sufentanil in children 5 months to 8.75 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Study ID   |Age [month(s)] |Body Weight [kg] |Observed AUC [µmol*min/l] |Predicted AUC [µmol*min/l] |Pred/Obs AUC Ratio |
|:----------|:--------------|:----------------|:-------------------------|:--------------------------|:------------------|
|Davis 1987 |1.29           |8.90             |2.14                      |1.16                       |0.54               |
|Davis 1987 |0.43           |5.30             |1.41                      |1.45                       |1.03               |
|Guay 1991  |2.08           |12.10            |0.28                      |0.17                       |0.60               |
|Guay 1991  |2.58           |16.00            |0.12                      |0.10                       |0.86               |
|Guay 1991  |2.67           |11.30            |0.23                      |0.26                       |1.13               |
|Guay 1991  |3.25           |16.00            |0.21                      |0.22                       |1.05               |
|Guay 1991  |3.83           |14.20            |0.17                      |0.14                       |0.84               |
|Guay 1991  |4.58           |15.00            |0.17                      |0.11                       |0.66               |
|Guay 1991  |4.58           |19.00            |0.35                      |0.22                       |0.63               |
|Guay 1991  |4.83           |17.50            |0.18                      |0.23                       |1.25               |
|Guay 1991  |5.25           |18.50            |0.11                      |0.12                       |1.04               |
|Guay 1991  |5.25           |19.65            |0.22                      |0.23                       |1.04               |
|Guay 1991  |5.33           |24.00            |0.35                      |0.29                       |0.83               |
|Guay 1991  |5.33           |24.00            |0.20                      |0.16                       |0.84               |
|Guay 1991  |5.75           |14.50            |0.39                      |0.20                       |0.50               |
|Guay 1991  |5.92           |28.20            |0.33                      |0.24                       |0.73               |
|Guay 1991  |5.92           |25.00            |0.15                      |0.12                       |0.84               |
|Guay 1991  |6.92           |29.60            |0.16                      |0.16                       |1.01               |
|Guay 1991  |7.50           |23.50            |0.09                      |0.07                       |0.77               |
|Guay 1991  |7.50           |15.20            |0.19                      |0.19                       |0.99               |
|Guay 1991  |8.75           |22.60            |0.15                      |0.14                       |0.93               |


Table 5: GMFE for Overall predictivity of the sufentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of sufentanil in children 5 months to 8.75 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Parameter |GMFE |
|:---------|:----|
|AUC       |1.25 |


Figure 2: Overall predictivity of the sufentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of sufentanil in children 5 months to 8.75 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


![](002_section_3/003_section_31/7-pk-ratio-plot-AUC.png)


Table 6: Measure of Overall predictivity of the sufentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of sufentanil in children 5 months to 8.75 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|                       | Number|Ratio |
|:----------------------|------:|:-----|
|Points Total           |     21|NA    |
|Points within 1.5-fold |     16|0.76  |
|Points within 2-fold   |     20|0.95  |





#### 1.4.1.1 Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.


Figure 3: Time Profile Analysis


![](002_section_3/004_section_32/3-Sufentanil-Pediatrics-Guay%201991%20patient%2011.png)


Figure 4: Time Profile Analysis 1


![](002_section_3/004_section_32/4-Sufentanil-Pediatrics-Guay%201991%20patient%2011.png)


Figure 5: Time Profile Analysis


![](002_section_3/004_section_32/5-Sufentanil-Pediatrics-Guay%201991%20patient%203.png)


Figure 6: Time Profile Analysis 1


![](002_section_3/004_section_32/6-Sufentanil-Pediatrics-Guay%201991%20patient%203.png)


Figure 7: Time Profile Analysis


![](002_section_3/004_section_32/7-Sufentanil-Pediatrics-Guay%201991%20patient%208.png)


Figure 8: Time Profile Analysis 1


![](002_section_3/004_section_32/8-Sufentanil-Pediatrics-Guay%201991%20patient%208.png)





### 1.4.2 Alfentanil model

Alfentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- den Hollander JM, Hennis PJ, Burm AG, Vletter AA, Bovill JG. Pharmacokinetics of alfentanil before and after cardiopulmonary bypass in pediatric patients undergoing cardiac surgery: Part I. J Cardiothorac Vasc Anesth. 1992 Jun;6(3):308-12.[[Meistelman 1987](#3-references)]
- Meistelman C, Saint-Maurice C, Lepaul M, Levron JC, Loose JP, Mac Gee K. A comparison of alfentanil pharmacokinetics in children and adults. Anesthesiology. 1987 Jan;66(1):13-6.[[den Hollander 1992](#3-references)]

The pediatric PBPK model predicted the AUC values of alfentanil observed in pediatric studies reasonably across all available age groups, ranging from 3.6 months to 9 years old. The ratios of mean predicted over observed AUC values are illustrated in the table below as well as in the predicted versus observed AUC ratio plot, showing that most predictions in children were within 2-fold error of observed values. Another reported study on alfentanil pharmacokinetics in children [[Goresky 1987](#3-references)] showed systematically higher exposure for most individuals compared to the other herein included studies. This deviation may have been caused by different impact of individual pathophysiology of the target study population, inaccurate in vitro assay-techniques or other study differences. 



Table 7: Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Study ID           |Age [year(s)] |Body Weight [kg] |Observed AUC [µmol*min/l] |Predicted AUC [µmol*min/l] |Pred/Obs AUC Ratio |
|:------------------|:-------------|:----------------|:-------------------------|:--------------------------|:------------------|
|den Hollander 1992 |0.92          |6.50             |50.66                     |50.01                      |0.99               |
|den Hollander 1992 |0.83          |6.40             |33.61                     |50.75                      |1.51               |
|den Hollander 1992 |0.99          |8.50             |47.54                     |54.22                      |1.14               |
|den Hollander 1992 |0.30          |5.10             |44.42                     |67.61                      |1.52               |
|den Hollander 1992 |0.92          |6.15             |38.17                     |42.72                      |1.12               |
|den Hollander 1992 |1.30          |10.40            |58.34                     |50.97                      |0.87               |
|den Hollander 1992 |9.00          |25.60            |27.13                     |46.58                      |1.72               |
|den Hollander 1992 |3.50          |14.40            |44.66                     |45.32                      |1.01               |
|den Hollander 1992 |5.50          |19.50            |49.70                     |45.40                      |0.91               |
|den Hollander 1992 |3.50          |18.50            |54.50                     |49.18                      |0.90               |
|Meistelman 1987    |4.70          |20.00            |14.12                     |9.82                       |0.70               |
|Meistelman 1987    |5.50          |20.00            |8.14                      |9.10                       |1.12               |
|Meistelman 1987    |7.70          |23.00            |5.79                      |9.06                       |1.57               |
|Meistelman 1987    |4.50          |14.00            |10.44                     |7.81                       |0.75               |
|Meistelman 1987    |4.80          |24.00            |12.98                     |11.61                      |0.89               |
|Meistelman 1987    |4.50          |20.00            |10.00                     |10.07                      |1.01               |
|Meistelman 1987    |6.20          |23.00            |10.91                     |9.86                       |0.90               |
|Meistelman 1987    |4.90          |22.00            |17.78                     |10.51                      |0.59               |


Table 8: GMFE for Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Parameter |GMFE |
|:---------|:----|
|AUC       |1.24 |


Figure 9: Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


![](002_section_3/005_section_33/11-pk-ratio-plot-AUC.png)


Table 9: Measure of Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|                       | Number|Ratio |
|:----------------------|------:|:-----|
|Points Total           |     18|NA    |
|Points within 1.5-fold |     13|0.72  |
|Points within 2-fold   |     18|1.00  |





#### 1.4.2.1 Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.


Figure 10: Time Profile Analysis


![](002_section_3/006_section_34/1-Alfentanil-Pediatrics-den%20Holländer%201992%20ind%203.png)


Figure 11: Time Profile Analysis 1


![](002_section_3/006_section_34/2-Alfentanil-Pediatrics-den%20Holländer%201992%20ind%203.png)





**Alfentanil-Model** Alfentanil-Model, Whole-body PBPK model of Alfentanil. (https://github.com/Open-Systems-Pharmacology/Alfentanil-Model) 

**Davis 1987** Davis PJ, Cook DR, Stiller RL, Davin-Robinson KA. Pharmacodynamics and pharmacokinetics of high-dose sufentanil in infants and children undergoing cardiac surgery. Anesth Analg. 1987 Mar;66(3):203-8.

**den Hollander 1992** den Hollander JM, Hennis PJ, Burm AG, Vletter AA, Bovill JG. Pharmacokinetics of alfentanil before and after cardiopulmonary bypass in pediatric patients undergoing cardiac surgery: Part I. J Cardiothorac Vasc Anesth. 1992 Jun;6(3):308-12.

**Edginton 2006** Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.

**Goresky 1987** Goresky GV, Koren G, Sabourin MA, Sale JP, Strunin L., The pharmacokinetics of alfentanil in children. Anesthesiology. 1987 Nov;67(5):654-9.

**Guay 1992** Guay J, Gaudreault P, Tang A, Goulet B, Varin F. Pharmacokinetics of sufentanil in normal children. Can J Anaesth. 1992 Jan;39(1):14-20.

**Maharaj 2013** Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.

**Meistelman 1987** Meistelman C, Saint-Maurice C, Lepaul M, Levron JC, Loose JP, Mac Gee K. A comparison of alfentanil pharmacokinetics in children and adults. Anesthesiology. 1987 Jan;66(1):13-6.

**Ontogeny Database** OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf (https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

**Sufentanil-Model** Sufentanil-Model, Whole-body PBPK model of Sufentanil. (https://github.com/Open-Systems-Pharmacology/Sufentanil-Model)


