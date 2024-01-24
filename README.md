# kingfish777.github.io
S. A. Malec's GitHub.io webpage
RESEARCH STATEMENT

I am an Assistant Professor in the Division of Translational Informatics at the University of New Mexico and an awardee of a K99/R00 “Pathway to Independence” grant (#R00LM013367) from the National Library of Medicine. My research focuses on improving the reliability of causal inference from observational health data. I develop methods incorporating background knowledge from the biomedical literature and ontologies to inform causal feature selection. The objective of causal feature selection is to idea sets of features optimized for causal estimation that reduce bias, including confounding and selection biases, thereby enhancing the overall validity and reliability of observational studies. My approach includes data-knowledge integration, empirical testing of bias reduction methods in observational studies, and exploring knowledge representations to optimize the causal feature selection process. My application areas include drug safety and Alzheimer’s dementia. However, my methods are generalizable to other areas, and I am interested in collaborating with others who find my work helpful. 

My approach involves three central themes: (I.) creating, curating, and improving existing representations of structured knowledge, (II.) translating epidemiological criteria into queries for searching structured knowledge for causal variables, and (III.) leveraging causal knowledge for causal discovery and estimating causal effects from observational data, e.g., electronic health records. My ongoing and future projects are arranged according to these themes:

# I. Creating, Curating, and Improving Existing Representations of Structured Knowledge

## ConfoundersOfModifiableRiskfActorsOfDEmentiadb (COMRADEdb): 

Noting inconsistencies in confounding control across studies, Blum et al. [2014] suggested the development of field-specific databases of confounders to improve the rigor and reproducibility of observational studies. Since no standardized reference database exists, the aim was to create one. Moreover, our work requires such a database to evaluate the results of the causal feature selection methods. This foundational work describes the development of a pilot database of confounders of modifiable risk factors of Alzheimer's disease. It is based on Cochrane Group recommendations for gathering data for conducting meta-reviews that assess the quality of confounding control in observational studies. In a pilot study, reported confounders were extracted from 59 observational studies cited in the Lancet Commission Report on Modifiable Risk Factors for Dementia by Livingston et al. [2017, 2020]. Preliminary findings were presented in a poster accepted at AMIA Summits 2023. Using a relational database to facilitate summarization, distinct patterns emerged in reported confounders. For example, prospective cohort studies report more behavioral variables, while retrospective patient health data tend to have more comorbidities. Because the manual extraction process is tedious, the manuscript includes a set of requirements for extracting the necessary data elements identified. The target journal for this paper is Nature Data. The submission timeline for this paper is October 2023. This paper will contribute to the development of systematized confounder selection and can be valuable for other researchers. 

## Future Work: 

In the summer of 2024, I plan to submit a grant proposal to the National Institute on Aging (NIA) through the R21 mechanism to expand COMRADEdb. This research project aims to accelerate the discovery process in this field by creating a database and a technical standard for sharing models that identify a comprehensive set of variables to collect data on to answer causal questions in research on risk factors of ADRD. The proposed grant will have three components. Firstly, I will develop an ecosystem to extend the coverage of COMRADEdb, scoping a more extensive set of observational studies from PubMed and EmBase, to acquire a more comprehensive coverage of confounders reported in the literature. Secondly, I will build an open causal modeling repository to facilitate the sharing of models. Finally, I will enable input and annotations from content experts in the National Academy of Sciences, Neuro-epidemiology subsection or who are faculty in relevant areas (e.g., neurology, psychiatry), using anonymized, IRB-approved survey questionnaires I developed with colleagues. This project aligns with the Division on Neuroscience’s (DN) focus on Alzheimer's disease.

# II. Translating Epidemiological Criteria into Queries for Searching Structured Knowledge for Causal Variables

## M-bias: 

I am working on addressing M-bias. M-bias can arise when adjusting for variables that are the effects of other variables connected to the exposure and outcome. In previous work, I developed causal feature selection methods that use structured knowledge to identify confounders, but it was uncertain which variables were implicated in M-bias. As a result, I developed methods to identify M-bias variables. The key steps of my method include searching for the causes of the exposure and outcome, searching for the effects of the causes of the exposure and outcome, and identifying common M-bias variables. I applied this method to identify variables implicated in M-bias scenarios for Alzheimer's disease and depression, among the twelve modifiable risk factors of dementia identified in the 2020 Lancet Commission report. Preliminary results showed that among 227 variables identified as confounders, 214 were also M-bias variables. I plan to submit a paper on this topic in the fall of 2024, building on my preliminary results presented at the AMIA Symposium 2022.


## Identifying Confounders for Depression and Dementia Subtypes Using Literature-Derived Structured Knowledge: A Preliminary Study:

This study aims to identify causal variables (e.g., confounders, colliders, mediators) for depression as the exposure and subtypes of dementia using literature-derived structured knowledge (SemMedDB v.43R as the source of literature-derived structured knowledge) and using the Venn diagram R package to visualize the outputs.  Causal variables delineate the foundational causal framework linking risk factors with distinct dementia subtypes. This investigation will yield significant insights into their respective etiologies. The acquired knowledge will subsequently inform and advance future research endeavors pertaining to dementia prevention and therapeutic interventions. For example, preliminary results show that the APP gene is a common confounder across many subtypes of dementia, and frontotemporal dementia (FTD) and early onset AD (EOAD) were the most distinct from the other dementia subtypes. I plan to apply these methods to analyze other modifiable risk factors of dementia and to evaluate the approach by comparing the confounders of different dementia subtypes from observational studies following the confounding control methodology developed in COMRADEdb. The journal Alzheimer’s and Dementia is the target venue for the Spring of 2024.

# III. Leveraging Causal Knowledge for Causal Discovery and Estimating Causal Effects from Observational Data

## Omitted variable bias: 

This research project focuses on addressing omitted variable bias (OVB) in causal inference. OVB arises when important variables are left out of an analysis, leading to inaccurate results. To address this, the project will leverage the knowledge of precision variables, which are determinants of the outcome, but not necessarily confounders, that can help reduce the impact of OVB. TMLE estimators have the property of being doubly robust and, if either the treatment or outcome models are complete, can account for model misspecification. The inclusion of precision variables will ensure that the inputs include a robust outcome model. In addition, because depression is a dynamic stochastic exposure and because there is time-varying confounding and confounders affected by prior treatment (CAPTs), we will test using incremental marginal structural models (MSMs) TMLE estimators described by Kennedy [2018]. Our ongoing research investigates the effect of depression on the risk of Alzheimer's disease using longitudinal data from electronic health records. Sensitivity analyses will be conducted using the E-value metric and a tiered approach to confounding control (see Albanese et al. [2014]) to assess the robustness of our results to residual biases. We plan to submit our findings to the Int Journ of Epi in the Winter 2023/2024.


## PACE project: 

The ongoing research aims to address M-bias in observational data in medical research by leveraging structured knowledge and causal discovery methods. The research seeks to investigate scientific questions about the effect of M-bias on drug safety, the first aim of my K99/R00. Since the literature and knowledge are incomplete, we intend to compare the impact of knowledge-driven M-bias identification methods with causal discovery methods for identifying M-bias on effect estimates from real-world data. This study uses well-characterized prospective cohort study design data from the Pennsylvania Pharmaceutical Assistance Contract for the Elderly (PACE) program. Since the effect of collider bias, including M-bias, is poorly understood, we will compare effect estimates by applying methods that prevent M-bias with estimates using variables identified by high-dimensional propensity score (HDPS) without correcting for M-bias or other colliders, as suggested by Scheeweiss et al. [2007]. We plan to submit our findings to the Journal Biomed Inf in the Fall of 2024.


## Future Work: 

In the short term, I plan to apply, develop, and improve causal feature selection methods and apply advanced estimators to measure the effects of other modifiable risk factors for AD from EHR data. Understanding the contribution of each modifiable risk factor will allow us to understand better how risk factors interact and to identify potential drug repurposing agents that minimize harm and optimize benefits. In June 2025, I plan to submit an R01 grant to the NIA, PCORI, or AHRQ to study comparative effectiveness and patient-centered outcomes of interventions aimed at modifiable risk factors for AD. In addition, I plan to seek funds to access AllofUs and UK BioBank data since these sources contain longitudinal patient health data, genetic biomarkers, sociodemographic data, and cognitive performance.
