 * [1 Pediatric Qualification Package: CYP3A4 Ontogeny](#1-pediatric-qualification-package-cyp3a4-ontogeny)
   * [1.1 Translation of Adult PBPK to Children](#11-translation-of-adult-pbpk-to-children)
   * [1.2 Anthropometric and Physiological Information ](#12-anthropometric-and-physiological-information-)
   * [1.3 Qualification of **CYP3A4 enzyme ontogeny**](#13-qualification-of-cyp3a4-enzyme-ontogeny)
   * [1.4 References](#14-references)
   * [1.5 Evaluation of Pediatric translation](#15-evaluation-of-pediatric-translation)
     * [1.5.1 Sufentanil model](#151-sufentanil-model)
       * [1.5.1.1 Concentration-Time Profiles](#1511-concentration-time-profiles)
     * [1.5.2 Alfentanil model](#152-alfentanil-model)
     * [1.5.3 References](#153-references)
       * [1.5.3.1 Concentration-Time Profiles](#1531-concentration-time-profiles)
   * [1.6 Evaluation of Adult PBPK models](#16-evaluation-of-adult-pbpk-models)
     * [1.6.1 Sufentanil adult PBPK model](#161-sufentanil-adult-pbpk-model)
     * [1.6.2 Compound: Sufentanil](#162-compound-sufentanil)
       * [1.6.2.1 Parameters](#1621-parameters)
       * [1.6.2.2 Calculation methods](#1622-calculation-methods)
       * [1.6.2.3 Processes](#1623-processes)
         * [1.6.2.3.1 Systemic Process: Glomerular Filtration-GFR](#16231-systemic-process-glomerular-filtration-gfr)
           * [1.6.2.3.1.1 Parameters](#162311-parameters)
         * [1.6.2.3.2 Metabolizing Enzyme: CYP3A4-Zhou et al. 2017](#16232-metabolizing-enzyme-cyp3a4-zhou-et-al-2017)
           * [1.6.2.3.2.1 Parameters](#162321-parameters)
     * [1.6.3 Sufentanil adult PBPK model performance](#163-sufentanil-adult-pbpk-model-performance)
       * [1.6.3.1 Concentration-Time Profiles](#1631-concentration-time-profiles)
     * [1.6.4 Alfentanil model](#164-alfentanil-model)
     * [1.6.5 References](#165-references)
     * [1.6.6 Compound: Alfentanil](#166-compound-alfentanil)
       * [1.6.6.1 Parameters](#1661-parameters)
       * [1.6.6.2 Calculation methods](#1662-calculation-methods)
       * [1.6.6.3 Processes](#1663-processes)
         * [1.6.6.3.1 Metabolizing Enzyme: CYP3A4-1st order CL](#16631-metabolizing-enzyme-cyp3a4-1st-order-cl)
           * [1.6.6.3.1.1 Parameters](#166311-parameters)
         * [1.6.6.3.2 Systemic Process: Glomerular Filtration-GFR](#16632-systemic-process-glomerular-filtration-gfr)
           * [1.6.6.3.2.1 Parameters](#166321-parameters)




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

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[1](#reference)]

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature, covering available dosing ranges for e.g. intravenous as well as oral administration, to capture both systemic clearance as well gut-wall metabolic clearance processes. For orally administered drugs, the same formulations that are used in children should ideally be included in the model for adults. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed area under the plasma concentration (AUC)-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children as in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity, intestinal permeability, solubility) were kept unchanged.

## 1.2 Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published [[2](#reference)]. The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The  applied ontogeny and variability of plasma proteins and active processes that are integrated into PK-Sim® for translation to children are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[3](#reference)] or otherwise referenced for the specific process.

## 1.3 Qualification of **CYP3A4 enzyme ontogeny**

To qualify the OSP suite for the pediatric translation of the pharmacokinetics of new drugs that are metabolized by CYP3A4, the following set of probe substances was included:

- Alfentanil [[4](#reference)]

- Sufentanil [[5](#reference)]

## 1.4 References

[1] [Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.](https://www.ncbi.nlm.nih.gov/pubmed/23344790)

[2] [Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.](https://www.ncbi.nlm.nih.gov/pubmed/16984214)

[3]  [OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf ](https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

[4] [Alfentanil-Model, Whole-body PBPK model of Alfentanil. https://github.com/Open-Systems-Pharmacology/Alfentanil-Model](https://github.com/incei/Alfentanil-Model)

[5] [Sufentanil-Model, Whole-body PBPK model of Sufentanil. https://github.com/Open-Systems-Pharmacology/Sufentanil-Model](https://github.com/incei/Sufentanil-Model)





## 1.5 Evaluation of Pediatric translation

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
|den Hollander 1992 |0.92          |6.50             |50.66                     |54.89                      |1.08               |
|den Hollander 1992 |0.83          |6.40             |33.61                     |55.63                      |1.66               |
|den Hollander 1992 |0.99          |8.50             |47.54                     |56.46                      |1.19               |
|den Hollander 1992 |0.30          |5.10             |44.42                     |73.46                      |1.65               |
|den Hollander 1992 |0.92          |6.15             |38.17                     |46.96                      |1.23               |
|den Hollander 1992 |1.30          |10.40            |58.34                     |56.16                      |0.96               |
|den Hollander 1992 |9.00          |25.60            |27.13                     |53.50                      |1.97               |
|den Hollander 1992 |3.50          |14.40            |44.66                     |50.68                      |1.13               |
|den Hollander 1992 |5.50          |19.50            |49.70                     |51.23                      |1.03               |
|den Hollander 1992 |3.50          |18.50            |54.50                     |54.94                      |1.01               |
|Meistelman 1987    |4.70          |20.00            |14.12                     |10.93                      |0.77               |
|Meistelman 1987    |5.50          |20.00            |8.14                      |10.15                      |1.25               |
|Meistelman 1987    |7.70          |23.00            |5.79                      |10.15                      |1.75               |
|Meistelman 1987    |4.50          |14.00            |10.44                     |8.67                       |0.83               |
|Meistelman 1987    |4.80          |24.00            |12.98                     |12.92                      |1.00               |
|Meistelman 1987    |4.50          |20.00            |10.00                     |11.20                      |1.12               |
|Meistelman 1987    |6.20          |23.00            |10.91                     |11.02                      |1.01               |
|Meistelman 1987    |4.90          |22.00            |17.78                     |11.71                      |0.66               |


Table 2: GMFE for Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Parameter |GMFE |
|:---------|:----|
|AUC       |1.25 |


Figure 1: Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/3-pk-ratio-plot-AUC.png)


Table 3: Measure of Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of all drugs in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|                       |Number |Ratio |
|:----------------------|:------|:-----|
|Points Total           |39     |NA    |
|Points within 1.5-fold |29     |0.74  |
|Points within 2-fold   |38     |0.97  |





### 1.5.1 Sufentanil model

Sufentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Davis PJ, Cook DR, Stiller RL, Davin-Robinson KA. Pharmacodynamics and pharmacokinetics of high-dose sufentanil in infants and children undergoing cardiac surgery. Anesth Analg. 1987 Mar;66(3):203-8.
- Guay J, Gaudreault P, Tang A, Goulet B, Varin F. Pharmacokinetics of sufentanil in normal children. Can J Anaesth. 1992 Jan;39(1):14-20.

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


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/003_Chapter%202_1_%20Sufentanil%20PK%20Ratio%20tables%20and%20Figures/7-pk-ratio-plot-AUC.png)


Table 6: Measure of Overall predictivity of the sufentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of sufentanil in children 5 months to 8.75 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|                       |Number |Ratio |
|:----------------------|:------|:-----|
|Points Total           |21     |NA    |
|Points within 1.5-fold |16     |0.76  |
|Points within 2-fold   |20     |0.95  |





#### 1.5.1.1 Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.


Figure 3: Time Profile Analysis


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/004_Chapter%202_2_%20Sufentanil%20Concentration_Time%20profiles%20in%20Children/9-Sufentanil-Guay%201991%20patient%2011.png)


Figure 4: Time Profile Analysis 1


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/004_Chapter%202_2_%20Sufentanil%20Concentration_Time%20profiles%20in%20Children/10-Sufentanil-Guay%201991%20patient%2011.png)


Figure 5: Time Profile Analysis


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/004_Chapter%202_2_%20Sufentanil%20Concentration_Time%20profiles%20in%20Children/11-Sufentanil-Guay%201991%20patient%203.png)


Figure 6: Time Profile Analysis 1


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/004_Chapter%202_2_%20Sufentanil%20Concentration_Time%20profiles%20in%20Children/12-Sufentanil-Guay%201991%20patient%203.png)


Figure 7: Time Profile Analysis


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/004_Chapter%202_2_%20Sufentanil%20Concentration_Time%20profiles%20in%20Children/13-Sufentanil-Guay%201991%20patient%208.png)


Figure 8: Time Profile Analysis 1


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/004_Chapter%202_2_%20Sufentanil%20Concentration_Time%20profiles%20in%20Children/14-Sufentanil-Guay%201991%20patient%208.png)





### 1.5.2 Alfentanil model

Alfentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- den Hollander JM, Hennis PJ, Burm AG, Vletter AA, Bovill JG. Pharmacokinetics of alfentanil before and after cardiopulmonary bypass in pediatric patients undergoing cardiac surgery: Part I. J Cardiothorac Vasc Anesth. 1992 Jun;6(3):308-12.
- Meistelman C, Saint-Maurice C, Lepaul M, Levron JC, Loose JP, Mac Gee K. A comparison of alfentanil pharmacokinetics in children and adults. Anesthesiology. 1987 Jan;66(1):13-6.

The pediatric PBPK model predicted the AUC values of alfentanil observed in pediatric studies reasonably across all available age groups, ranging from 3.6 months to 9 years old. The ratios of mean predicted over observed AUC values are illustrated in the table below as well as in the predicted versus observed AUC ratio plot, showing that most predictions in children were within 2-fold error of observed values. Another reported study on alfentanil pharmacokinetics in children [1] showed systematically higher exposure for most individuals compared to the other herein included studies. This deviation may have been caused by different impact of individual pathophysiologies of the target study population, inaccurate in vitro assay-techniques or other study differences. 

### 1.5.3 References

[1] Goresky GV, Koren G, Sabourin MA, Sale JP, Strunin L., The pharmacokinetics of alfentanil in children. Anesthesiology. 1987 Nov;67(5):654-9.


Table 7: Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Study ID           |Age [year(s)] |Body Weight [kg] |Observed AUC [µmol*min/l] |Predicted AUC [µmol*min/l] |Pred/Obs AUC Ratio |
|:------------------|:-------------|:----------------|:-------------------------|:--------------------------|:------------------|
|den Hollander 1992 |0.92          |6.50             |50.66                     |54.89                      |1.08               |
|den Hollander 1992 |0.83          |6.40             |33.61                     |55.63                      |1.66               |
|den Hollander 1992 |0.99          |8.50             |47.54                     |56.46                      |1.19               |
|den Hollander 1992 |0.30          |5.10             |44.42                     |73.46                      |1.65               |
|den Hollander 1992 |0.92          |6.15             |38.17                     |46.96                      |1.23               |
|den Hollander 1992 |1.30          |10.40            |58.34                     |56.16                      |0.96               |
|den Hollander 1992 |9.00          |25.60            |27.13                     |53.50                      |1.97               |
|den Hollander 1992 |3.50          |14.40            |44.66                     |50.68                      |1.13               |
|den Hollander 1992 |5.50          |19.50            |49.70                     |51.23                      |1.03               |
|den Hollander 1992 |3.50          |18.50            |54.50                     |54.94                      |1.01               |
|Meistelman 1987    |4.70          |20.00            |14.12                     |10.93                      |0.77               |
|Meistelman 1987    |5.50          |20.00            |8.14                      |10.15                      |1.25               |
|Meistelman 1987    |7.70          |23.00            |5.79                      |10.15                      |1.75               |
|Meistelman 1987    |4.50          |14.00            |10.44                     |8.67                       |0.83               |
|Meistelman 1987    |4.80          |24.00            |12.98                     |12.92                      |1.00               |
|Meistelman 1987    |4.50          |20.00            |10.00                     |11.20                      |1.12               |
|Meistelman 1987    |6.20          |23.00            |10.91                     |11.02                      |1.01               |
|Meistelman 1987    |4.90          |22.00            |17.78                     |11.71                      |0.66               |


Table 8: GMFE for Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|Parameter |GMFE |
|:---------|:----|
|AUC       |1.26 |


Figure 9: Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/005_Chapter%202_3_%20Alfentanil%20PK%20Ratio%20tables%20and%20Figures/11-pk-ratio-plot-AUC.png)


Table 9: Measure of Overall predictivity of the alfentanil PBPK model. Open circles represent mean ratios of PBPK predicted AUC over observed AUC of alfentanil in children 3.6 months to 9 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.


|                       |Number |Ratio |
|:----------------------|:------|:-----|
|Points Total           |18     |NA    |
|Points within 1.5-fold |13     |0.72  |
|Points within 2-fold   |18     |1.00  |





#### 1.5.3.1 Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.


Figure 10: Time Profile Analysis


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/006_Chapter%202_4_%20Alfentanil%20Concentration_Time%20profiles%20in%20Children/1-Alfentanil-den%20Holländer%201992%20ind%203.png)


Figure 11: Time Profile Analysis 1


![](002_Chapter%202_%20Pediatric%20translation%20qualification%20results/006_Chapter%202_4_%20Alfentanil%20Concentration_Time%20profiles%20in%20Children/2-Alfentanil-den%20Holländer%201992%20ind%203.png)





## 1.6 Evaluation of Adult PBPK models

The PBPK models of **sufentanil** and **alfentanil** were developed with clinical pharmacokinetic data covering at least administrations given in children. Plasma concentrations following intravenous administration, oral administration, multiple dose application, fractions excreted to urine or bile and other clinical measurements were included for model development whenever available. 






### 1.6.1 Sufentanil adult PBPK model

Sufentanil is a potent synthetic opioid. Like other opioids, sufentanil creates a stable hemodynamic environment in cardiovascularly compromised pediatric patients. Sufentanil has a high lipid solubility, which accounts for the fast onset when given intravenously. The commercial solution comes as preservative-free sufentanil citrate, injectable with a pH of 4.5–7.0 (Jansen-Cilag AB, Sweden). Sufentanil is solely metabolised by CYP3A4. Due to the high hepatic extraction ratio, for the overall clearance of sufentanil both CYP3A4 values as well as liver blood flow rate play dominant roles in the elimination in adult populations. The final sufentanil model applies metabolism by CYP3A4 and glomerular filtration and adequately described the pharmacokinetics of sufentanil in adults.

The Sufentanil model was developed using data of the following publications:

- Bovill JG, Sebel PS, Blackburn CL, Oei-Lim V, Heykants JJ. The pharmacokinetics of sufentanil in surgical patients. Anesthesiology. 1984 Nov;61(5):502-6. (https://www.ncbi.nlm.nih.gov/pubmed/6238552)
- Willsie SK, Evashenk MA2, Hamel LG, Hwang SS, Chiang YK, Palmer PP. Pharmacokinetic properties of single- and repeated-dose sufentanil sublingual tablets in healthy volunteers. Clin Ther. 2015 Jan 1;37(1):145-55. doi: 10.1016/j.clinthera.2014.11.001. Epub 2014 Dec 24.
(https://www.ncbi.nlm.nih.gov/pubmed/25544247)

The compound properties used for input are illustrated below.


### 1.6.2 Compound: Sufentanil

#### 1.6.2.1 Parameters

Name                                       | Value                | Value Origin                                      | Alternative              | Default
------------------------------------------ | -------------------- | ------------------------------------------------- | ------------------------ | -------
Solubility at reference pH                 | 0.076 mg/l           | Internet-Other-ROY,SD & FLYNN,GL (1988)           | ROY,SD & FLYNN,GL (1988) | True   
Reference pH                               | 7                    | Internet-Other-ROY,SD & FLYNN,GL (1988)           | ROY,SD & FLYNN,GL (1988) | True   
Lipophilicity                              | 2.896 Log Units      | Parameter Identification-Parameter Identification | Fitted LogP              | True   
Fraction unbound (plasma, reference value) | 0.075                | Publication-Zhou et al. 2017                      | Zhou et al. 2017         | True   
Is small molecule                          | Yes                  |                                                   |                          |        
Molecular weight                           | 386.6 g/mol          | Publication-Zhou et al. 2017                      |                          |        
Plasma protein binding partner             | a1-acid glycoprotein |                                                   |                          |        
#### 1.6.2.2 Calculation methods

Name                    | Value          
----------------------- | ---------------
Partition coefficients  | Schmitt        
Cellular permeabilities | PK-Sim Standard
#### 1.6.2.3 Processes

##### 1.6.2.3.1 Systemic Process: Glomerular Filtration-GFR

Species: Human
###### 1.6.2.3.1.1 Parameters

Name         | Value | Value Origin                
------------ | -----:| ----------------------------
GFR fraction |     1 | Publication-Zhou et al. 2017
##### 1.6.2.3.2 Metabolizing Enzyme: CYP3A4-Zhou et al. 2017

Species: Human
Molecule: CYP3A4
###### 1.6.2.3.2.1 Parameters

Name                | Value              | Value Origin                                     
------------------- | ------------------ | -------------------------------------------------
Intrinsic clearance | 9.6138746106 l/min | Parameter Identification-Parameter Identification





### 1.6.3 Sufentanil adult PBPK model performance

Below you find the input goodness-of-fit visual diagnostic plots for sufentanil PBPK model performance (observed versus individually simulated plasma concentration and weighted residuals versus time) of all adult data.



Figure 12: Goodness-of-fit visual diagnostic plots of the sufentanil PBPK model performance: observed versus individually predicted plasma concentration versus time of all adult data.


![](007_Chapter%203_%20Adult%20PBPK%20model%20building%20and%20performance/009_Chapter%203_2_%20Sufentanil%20Diagnostics%20Plots/GOFMergedPlot-1-predictedVsObserved.png)


Figure 13: Goodness-of-fit visual diagnostic plots of the sufentanil PBPK model performance: weighted residuals versus time of all adult data.


![](007_Chapter%203_%20Adult%20PBPK%20model%20building%20and%20performance/009_Chapter%203_2_%20Sufentanil%20Diagnostics%20Plots/GOFMergedPlot-2-residualsOverTime.png)





#### 1.6.3.1 Concentration-Time Profiles

Simulated versus observed plasma concentration-time profiles of all data are listed below.


Figure 14: Time Profile Analysis


![](007_Chapter%203_%20Adult%20PBPK%20model%20building%20and%20performance/010_Chapter%203_3_%20Sufentanil%20Concentration_Time%20profiles%20in%20Adults/3-Sufentanil-Bovill%201984.png)


Figure 15: Time Profile Analysis 1


![](007_Chapter%203_%20Adult%20PBPK%20model%20building%20and%20performance/010_Chapter%203_3_%20Sufentanil%20Concentration_Time%20profiles%20in%20Adults/4-Sufentanil-Bovill%201984.png)


Figure 16: Time Profile Analysis


![](007_Chapter%203_%20Adult%20PBPK%20model%20building%20and%20performance/010_Chapter%203_3_%20Sufentanil%20Concentration_Time%20profiles%20in%20Adults/7-Sufentanil-Taverne%201992%20(for%20reporting).png)


Figure 17: Time Profile Analysis 1


![](007_Chapter%203_%20Adult%20PBPK%20model%20building%20and%20performance/010_Chapter%203_3_%20Sufentanil%20Concentration_Time%20profiles%20in%20Adults/8-Sufentanil-Taverne%201992%20(for%20reporting).png)





### 1.6.4 Alfentanil model

Alfentanil is another potent, short-acting synthetic opioid analgesic drug, used for anaesthesia in surgery, which is solely metabolized by CYP3A4, with less than 1% of an alfentanil dose being excreted unchanged in urine after intravenous administration. The model has been build and evaluated in healthy adults and published by Hanke et al. [1] The model applies metabolism by CYP3A4 and glomerular filtration. The alfentanil PBPK model adequately described the pharmacokinetics of alfentanil in adults. Additionally the model has been republished and fully described including evaluation documentation of the adult PBPK model in Github under 'https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/tree/v2.0' [2].

### 1.6.5 References

[1] Hanke N, Frechen S, Moj D, Britz H, Eissing T, Wendl T, Lehr T. PBPK models for CYP3A4 and P-gp DDI prediction: a modeling network of rifampicin, itraconazole, clarithromycin, midazolam, alfentanil and digoxin. CPT: Pharmacometrics & Systems Pharmacology (2018), https://doi.org/10.1002/psp4.12343.

[2] https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/tree/v2.0

The compound properties used for input are illustrated below.


### 1.6.6 Compound: Alfentanil

#### 1.6.6.1 Parameters

Name                                             | Value                   | Value Origin                                                                                                          | Alternative | Default
------------------------------------------------ | ----------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------- | -------
Solubility at reference pH                       | 992 mg/l                | Publication-Hanke 2018                                                                                                | Baneyx 2014 | True   
Reference pH                                     | 6.5                     | Publication-Hanke 2018                                                                                                | Baneyx 2014 | True   
Lipophilicity                                    | 1.8463211883 Log Units  | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Fit         | True   
Fraction unbound (plasma, reference value)       | 0.1                     | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Healthy     | True   
Permeability                                     | 0.0068752756625 cm/min  | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Optimized   | True   
Specific intestinal permeability (transcellular) | 0.00057373577138 cm/min | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Optimized   | True   
Is small molecule                                | Yes                     |                                                                                                                       |             |        
Molecular weight                                 | 416.52 g/mol            | Publication-Drugbank                                                                                                  |             |        
Plasma protein binding partner                   | a1-acid glycoprotein    |                                                                                                                       |             |        
#### 1.6.6.2 Calculation methods

Name                    | Value              
----------------------- | -------------------
Partition coefficients  | Rodgers and Rowland
Cellular permeabilities | PK-Sim Standard    
#### 1.6.6.3 Processes

##### 1.6.6.3.1 Metabolizing Enzyme: CYP3A4-1st order CL

Species: Human
Molecule: CYP3A4
###### 1.6.6.3.1.1 Parameters

Name                | Value              | Value Origin                                                                                                         
------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------
Intrinsic clearance | 0.5272297928 l/min | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28
##### 1.6.6.3.2 Systemic Process: Glomerular Filtration-GFR

Species: Human
###### 1.6.6.3.2.1 Parameters

Name         | Value | Value Origin          
------------ | -----:| ----------------------
GFR fraction |  0.06 | Publication-Hanke 2018


