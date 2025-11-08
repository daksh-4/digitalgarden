---
{"dg-publish":true,"permalink":"/research/understanding-trends-in-the-prescribing-of-thrombolytic-agents-throughout-england-a-time-series-analysis/","noteIcon":""}
---


**Abstract**

This report explores variation in the prescribing of two thrombolytic agents (tenecteplase and alteplase) used in the management of acute ischaemic stroke. It provides a comprehensive analysis of prescribing patterns following the July 2024 NICE guidance update, covering the use of thrombolytic agents in the management of ischaemic stroke. Tenecteplase had almost no usage before the guidance update, however, after July 2024 there has been substantial variation in uptake amongst integrated care boards (ICBs), with some ICBs rapidly switching whilst others (particularly London-based ICBs) have lagged behind despite hosting clinical trials investigating tenecteplase’s suitability. In this report, we have outlined the implication of missed opportunities for both cost savings (approximately £384 per treatment) and improved access to thrombolytic treatment, highlighting the need for better understanding of implementation barriers in the National Health Service (NHS). We found a clear national shift towards tenecteplase adoption, with potential savings of ~£3 million in drug costs only if all doses had been switched after the guidance update. Analysis of ICB-level data revealed that adoption speed was not driven by ICB size, existing thrombolysis rates, or stroke care quality, but perhaps instead by distinct organisational capabilities and decision-making processes within each region.

**Introduction**

Thrombolytic therapy has transformed outcomes across cardiovascular medicine over the past three decades, dramatically reducing mortality and morbidity in myocardial infarction, acute ischaemic stroke and pulmonary embolism 1,2,3. While thrombolysis revolutionised acute coronary syndrome management in the 1980s and 1990s, the widespread adoption of primary percutaneous coronary intervention has largely supplanted its use in myocardial infarction 4. Similarly, catheter-directed thrombolysis for pulmonary embolism remains reserved for selected high-risk cases 5. In 2025, acute ischaemic stroke represents the predominant indication for systemic thrombolytic therapy in the NHS and currently 14% of all stroke patients receive thrombolysis 6.

Since the 1990s, alteplase has served as the established standard of care for thrombolytic therapy in acute ischaemic stroke. The emergence of tenecteplase, which was licensed for use in acute ischaemic stroke in April 2024, presents a potential alternative that has created new opportunities in stroke care delivery. Tenecteplase is a modified plasminogen activator that offers potential advantages over alteplase through single-bolus administration (reducing nursing time), improved storage stability whilst maintaining comparable efficacy and no significant increases in adverse events7. In the UK, its efficacy was assessed in the ATTEST-2 trial, which demonstrated non-inferiority to alteplase via modified Rankin Scale score distribution8. Whilst there were numerically higher numbers of haemorrhagic events in the tenecteplase group compared to the alteplase group, this number was not statistically significant. In the TWIST trial, the number of intracranial haemorrhages was similar to previous trials of wake-up stroke patients, providing more reassurance on safety outcomes9. Updated NICE guidance in July 2024 recommends tenecteplase as a suitable, cheaper alternative to alteplase with equivalent outcomes and safety. The evidence for this guidance change was based on two clinical trials, AcT10 and EXTEND-IA TNK Part 111. In the AcT trial, intravenous tenecteplase (0.25 mg/kg) was found to be non-inferior to alteplase (0.9 mg/kg) for achieving a modified Rankin Scale score of 0-1 at 90-120 days with similar rates of symptomatic intracerebral haemorrhage and 90-day mortality. In the EXTEND-IA TNK trial, tenecteplase before thrombectomy led to substantially higher rates of early reperfusion than alteplase and a better median 90-day modified Rankin Scale score with no significant difference in symptomatic intracerebral haemorrhage.

The prospect of single-bolus administration also confers some unique advantages. Thrombolysis can be started at presentation to regional/non-specialist hospitals before transfer to Hyperacute Stroke Units (HASUs) for thrombectomy or further care, without the need for setting up infusions that would need to be maintained during transport. As several ICBs shift to the HASU model of stroke care where all patients are transferred to specialist centres, tenecteplase provides a unique avenue in the "drip and ship" route of stroke management.

Switching to tenecteplase has been encouraged, given its lower cost than alteplase, comparable outcomes and ease of administration. This report addresses three key objectives: first, we assess whether significant changes in prescribing have occurred nationally following the NICE guidance update and quantify the magnitude of regional variation in adoption patterns across ICBs. Second, we examine organisational characteristics such as ICB size, stroke unit performance and thrombolysis rates to identify factors associated with adoption speed. Third, we calculate the potential cost implications of varying adoption rates across the NHS.

**Methodology**

**Study design**

We conducted an interrupted time series analysis (ITSA) of secondary care drug pharmacy stock control data to evaluate the impact of the NICE guidance update on tenecteplase and alteplase prescribing.

**Data source**

OpenPrescribing hospitals data were used to look at national and regional trends in thrombolytic prescribing. The information on this platform is based on the Secondary Care Medicines Dataset (SCMD), which provides monthly prescribing information for NHS Trusts in England. For further analysis, prescription volumes of alteplase and tenecteplase were extracted over a 24-month study period from July 2023 to June 2025 from publicly available datasets, encompassing 12 months before and after the NICE guidance change (July 2024). Full description of the organisation within the SCMD can be found in the appendix.

**Data aggregation**

For comparisons between alteplase and tenecteplase, we calculated defined daily doses (DDDs), which is a standardised measurement by the World Health Organisation (WHO) for the average maintenance dose of a drug taken per day for its main indication in adults. Alteplase is dosed at 0.9 mg/kg (maximum 90 mg) delivered as an infusion over 60 minutes, yielding a WHO DDD of 100 mg for an average adult (~80-90 kg). Tenecteplase is administered as a single weight-tiered bolus (25-50 mg depending on body weight), corresponding to a DDD of 40mg (8,000 units) for tenecteplase. ICB level aggregation was chosen due to small numbers in trust level data. We also corrected for ICB size by dividing DDD numbers by total number of patients registered to GPs within each ICB.

**Outline of time series analysis**

An interrupted time series analysis was employed to assess the impact of the July 2024 NICE guidance change on prescribing patterns. ITSA is well-suited to evaluating longitudinal effects of population-level interventions where randomisation is not feasible. Model specification can be found in the appendix.

Autocorrelation is common in ITSA data due to the temporal structure of repeated measures. To support valid inference, we applied Newey-West heteroskedasticity and autocorrelation-consistent (HAC) standard errors. This approach adjusts the variance-covariance matrix of the estimated coefficients, providing robust standard errors under both autocorrelation and heteroskedasticity. We implemented a systematic approach to lag selection by fitting multiple models with different lag lengths and comparing their performance using information criteria, settling on a lag length of 3. Model diagnostics were performed by examining residual plots for patterns, and conducting Durbin-Watson tests to assess residual autocorrelation. Visual inspection of fitted values against observed data confirmed appropriate model specification across ICBs.

ICBs were organised into 3 categories based on slope change to characterise changes in prescribing behaviour. Green indicates significant p-values <0.05, orange indicates p-values in the range 0.05-0.1 as borderline and red indicates p-values >0.1. The basis of ranking ICBs on changes to prescribing was by slope change (calculated as : |slope gradient prior to July 2024 – slope gradient after July 2024|).

**Pricing**

To create a proxy cost per DDD, we divided the summed total expenditure nationally in the “indicative cost” column of SCMD by the summed total number of DDDs stored in the 24 month period; acknowledging that the indicative cost does not necessarily represent the actual price paid for medications.

**Baseline characteristics on stroke management**

To ensure valid comparison of baseline characteristics, we used the Sentinel Stroke National Audit Programme (SSNAP) to benchmark stroke management metrics across ICBs. SSNAP is a comprehensive, longitudinal clinical audit that captures data on all stroke patients treated in acute hospitals across England, Wales, and Northern Ireland, following their care through to six months post-stroke. SSNAP’s primary aims are to benchmark stroke services regionally and nationally, monitor progress amid NHS organisational change, support clinicians in identifying and implementing improvements, and empower patients through transparent reporting. Each year, data from over 90,000 patients, representing more than 90% of stroke admissions to NHS hospitals, are submitted, ensuring high completeness and reliability. SSNAP also publishes results every 3 months, which is the data we used to collate key indicators of stroke care, particularly total number of stroke patients admitted, ratio of patients thrombolysed and ratio of patients that spent more than 90% of their time in hospital admitted in a stroke unit.

All analyses were conducted in R version 4.3.1.

**Results**

**Study cohort and prescribing volumes**

Between July 2023 and June 2025, we analysed prescribing data from 42 ICBs across NHS England. Over the 24-month study period, a total of 31,320 DDDs of thrombolytic agents were prescribed, comprising 26,083 DDDs of alteplase and 5,237 DDDs of tenecteplase.

**National prescribing trends**


![tenecteplase](/img/user/6-Main-Notes/7-Attachments/tenecteplase.png)

Figure 1 Visualisation of prescribing trends in NHS regions of alteplase (left) and tenecteplase (right)

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%201.png>)

Figure 2 National Prescribing trends

Figure 2 shows a clear change in prescribing trends nationally since the introduction of the NICE guidelines in July of 2024. The biggest jump in tenecteplase usage was September to October 2024, 2 months after the new guideline update. Broadly the rate of decline in alteplase usage seems to match the rate of uptake of tenecteplase, hinting that the national response to the guidance is to start replacing alteplase usage with tenecteplase. Furthermore, the most recent data shows that tenecteplase usage is beginning to overtake alteplase usage.

Analyses via the OpenPrescribing Hospitals platform showed significant regional variation with a general trend of uptake in tenecteplase post July 2024 and decline in alteplase usage over the same period.

**Interrupted time series analysis: Alteplase**

The interrupted time series analysis for alteplase demonstrated statistically significant post-intervention slope changes across the majority of ICBs after the NICE guidance update (Table 2). Pre-intervention slope coefficients (β₁) were generally small, indicating stable baseline prescribing trends. The immediate level change at July 2024 (β₂) was variable but modest in magnitude across most ICBs, suggesting that the transition did not occur as an abrupt step change but rather evolved progressively over subsequent months.

Post-intervention slope coefficients (β₃) were overwhelmingly negative, reflecting sustained reductions in alteplase usage following the NICE guidance update. The ICBs demonstrating the largest and most statistically significant reductions in alteplase prescribing were Mid and South Essex (β₃ = -0.0336, p < 0.001), Shropshire Telford and Wrekin (β₃ = -0.0286, p = 0.003), Dorset (β₃ = -0.0256, p < 0.001), Norfolk and Waveney (β₃ = -0.0226, p < 0.001), and Lancashire and South Cumbria (β₃ = -0.0228, p < 0.001). These regions exhibited steep negative trajectories, indicative of near-complete formulary switches.

In contrast, several ICBs showed minimal or non-significant changes in alteplase prescribing post-intervention. Greater Manchester (β₃ = -0.0016, p = 0.600), North West London (β₃ = -0.0006, p = 0.857), Leicester Leicestershire and Rutland (β₃ = 0.0013, p = 0.700), and North Central London (β₃ = 0.0049, p = 0.083) demonstrated persistently flat or even slightly positive slopes, suggesting resistance to formulary transition or delayed implementation. Notably, Devon exhibited a non-significant positive post-intervention slope (β₃ = 0.0049, p = 0.157), diverging from the national trend.

**Interrupted time series analysis: Tenecteplase**

Tenecteplase prescribing exhibited the inverse pattern to alteplase, with predominantly positive post-intervention slopes across ICBs (Table 3). Many ICBs had zero or near-zero tenecteplase usage in the pre-intervention period, consistent with tenecteplase’s recent licensure and lack of prior guideline endorsement

The ICBs with the largest and most statistically significant increases in tenecteplase prescribing post-intervention mirrored those with the steepest alteplase reductions: Shropshire Telford and Wrekin (β₃ = 0.0290, p < 0.001), Mid and South Essex (β₃ = 0.0260, p < 0.001), Dorset (β₃ = 0.0235, p < 0.001), Lancashire and South Cumbria (β₃ = 0.0233, p < 0.001), and Norfolk and Waveney (β₃ = 0.0189, p < 0.001). These findings indicate coordinated formulary transitions within these regions, with reductions in one agent directly corresponding to increases in the other.

Several ICBs demonstrated substantial tenecteplase uptake despite not being among the fastest alteplase reducers. Bath and North East Somerset Swindon and Wiltshire (β₃ = 0.0158, p < 0.001), Somerset (β₃ = 0.0179, p < 0.001), and North East and North Cumbria (β₃ = 0.0148, p < 0.001) all showed strong positive slopes, suggesting proactive adoption. North East and North Cumbria's uptake is particularly notable given its status as the largest ICB by stroke volume, indicating that scale did not impede implementation.

Conversely, several ICBs exhibited minimal tenecteplase uptake despite significant time elapsed post-guidance. North Central London showed a non-significant negative slope (β₃ = -0.0007, p = 0.451), and Cambridgeshire and Peterborough demonstrated a significant negative slope (β₃ = -0.0062, p = 0.039), both diverging from the national trend. London ICBs more broadly—including North West London (β₃ = 0.0076, p = 0.001), North Central London, South West London (β₃ = 0.0034, p = 0.080), South East London (β₃ = 0.0069, p = 0.039), and North East London (β₃ = 0.0096, p < 0.001) demonstrated consistently slower uptake compared to the national average, despite North Central London having hosted the ATTEST-2 trial.

**ICB baseline characteristics and predictors of adoption**

ICB-level baseline characteristics also exhibited considerable heterogeneity. The largest ICBs by registered GP population were North East and North Cumbria (77.2 million), Greater Manchester (78.5 million), and Cheshire and Merseyside (66.7 million), which also reported the highest stroke admission volumes (12,630, 9,485, and 8,775 admissions respectively). Median thrombolysis rates were approximately 14% (IQR 0.11-0.16), ranging from 5% in Cornwall and the Isles of Scilly to 23% in Buckinghamshire Oxfordshire and Berkshire West. The proportion of patients spending at least 90% of their stay on stroke units varied from 47% in Lincolnshire to 88% in Kent and Medway.

To assess whether organisational capacity or stroke care quality influenced adoption speed, we examined correlations between ITSA-derived slope changes and baseline metrics. Notably, ICBs with the highest baseline thrombolysis rates did not demonstrate the fastest tenecteplase adoption. Frimley and Buckinghamshire Oxfordshire and Berkshire West, despite leading in thrombolysis ratios, ranked only 18th and 17th for adoption speed respectively. Conversely, Dorset (thrombolysis rate 0.13) and Shropshire Telford and Wrekin (0.18) ranked 3rd and 1st despite below- or mid-range baseline rates.

Similarly, stroke unit quality showed no correlation with adoption. Kent and Medway, Hertfordshire and West Essex, and Hampshire and Isle of Wight had the highest ratio of patients spending 90% of their stay in the stroke unit ranked only 12th, 36th and 34th for tenecteplase adoption. In contrast, Dorset and Shropshire Telford and Wrekin achieved rapid adoption despite lower stroke unit performance metrics (0.65 and 0.68 respectively).

ICB size was also not a clear predictor of adoption patterns. While North East and North Cumbria (largest ICB, 12,630 admissions) ranked 8th for adoption, Greater Manchester (second-largest, 9,485 admissions) ranked second last (41st). Smaller ICBs like Shropshire Telford and Wrekin (1,503 admissions) and Dorset (3,355 admissions) led adoption nationally. However, when analyzing absolute prescribing changes without GP population correction, North East and North Cumbria demonstrated the greatest slope change, and Greater Manchester rose into the top 10, suggesting that large ICBs are adopting tenecteplase in substantial absolute volumes, but this adoption appears modest when standardised for patient volume. This distinction highlights that large ICBs may be implementing change effectively in absolute terms while smaller ICBs achieve proportionally greater shifts in practice patterns. These findings indicate that neither stroke care quality metrics, thrombolysis rates, nor organisational size alone determine implementation speed.

|   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|
|ICB Name|Registered GP Patients|Stroke Admissions|Median thrombolysis rates with IQR|Median ratio of patients spending 90% of stay in a stroke unit with IQR|Total Alteplase DDDs|Total Tenecteplase DDDs|
|Bath And North East Somerset Swindon And Wiltshire|24146635|3042|0.1 [0.08–0.11]|0.75 [0.74–0.78]|412.28|103.75|
|Bedfordshire Luton And Milton Keynes|27209574|2189|0.18 [0.18–0.2]|0.79 [0.76–0.81]|512.58|75|
|Birmingham And Solihull|39146812|5332|0.08 [0.07–0.1]|0.68 [0.67–0.69]|635.26|84.375|
|Black Country|31964323|3192|0.14 [0.11–0.14]|0.71 [0.65–0.73]|482.82|120|
|Bristol North Somerset And South Gloucestershire|26123593|2708|0.16 [0.13–0.16]|0.79 [0.68–0.82]|353.12|46.25|
|Buckinghamshire Oxfordshire And Berkshire West|47968152|4209|0.23 [0.22–0.23]|0.83 [0.82–0.85]|965.06|209.375|
|Cambridgeshire And Peterborough|25171586|3386|0.18 [0.17–0.2]|0.61 [0.6–0.66]|564.84|163.75|
|Cheshire And Merseyside|66748976|8775|0.15 [0.15–0.16]|0.82 [0.79–0.83]|1292.7224|271.25|
|Cornwall And The Isles Of Scilly|14509332|1704|0.05 [0.05–0.09]|0.72 [0.7–0.75]|160.260475|41.25|
|Coventry And Warwickshire|26550849|2152|0.13 [0.11–0.16]|0.82 [0.8–0.83]|472.52|60.625|
|Derby And Derbyshire|27255723|3640|0.09 [0.08–0.09]|0.7 [0.67–0.73]|379.92|76.875|
|Devon|31048202|5112|0.12 [0.12–0.13]|0.78 [0.76–0.81]|647|41.875|
|Dorset|19944562|3355|0.13 [0.12–0.14]|0.65 [0.63–0.71]|365.72|116.875|
|Frimley|20264524|1300|0.2 [0.19–0.26]|0.81 [0.79–0.84]|71.03|96.875|
|Gloucestershire|16606101|1749|0.11 [0.1–0.12]|0.84 [0.83–0.84]|200.5|60.625|
|Greater Manchester|78512464|9485|0.12 [0.11–0.13]|0.84 [0.82–0.84]|1757.2|124.375|
|Hampshire And Isle Of Wight|47112369|5967|0.19 [0.17–0.19]|0.85 [0.85–0.86]|835.82|371.875|
|Herefordshire And Worcestershire|19922099|2382|0.12 [0.11–0.14]|0.77 [0.71–0.77]|302.54|137.5|
|Hertfordshire And West Essex|39690879|2829|0.13 [0.11–0.15]|0.85 [0.84–0.89]|476.08|66.25|
|Humber And North Yorkshire|43339819|6050|0.16 [0.15–0.17]|0.8 [0.78–0.83]|980.92|136.25|
|Kent And Medway|48512710|5105|0.16 [0.15–0.17]|0.88 [0.87–0.88]|781|248.75|
|Lancashire And South Cumbria|44552932|5778|0.14 [0.12–0.16]|0.81 [0.79–0.83]|928.6|216.25|
|Leicester Leicestershire And Rutland|29441426|2268|0.15 [0.14–0.16]|0.77 [0.74–0.78]|428.94|110|
|Lincolnshire|19714080|1771|0.11 [0.1–0.11]|0.47 [0.44–0.48]|218.84|39.375|
|Mid And South Essex|30832947|3666|0.17 [0.15–0.18]|0.81 [0.78–0.82]|857.78|223.125|
|Norfolk And Waveney|26308890|3501|0.15 [0.15–0.17]|0.74 [0.72–0.78]|639.34|113.125|
|North Central London|43564292|3018|0.11 [0.11–0.12]|0.67 [0.66–0.72]|774.180425|20|
|North East And North Cumbria|77153663|12630|0.15 [0.14–0.16]|0.86 [0.84–0.87]|1668.26|419.375|
|North East London|58919443|5752|0.16 [0.16–0.17]|0.78 [0.77–0.79]|792.2|173.75|
|North West London|69291292|7114|0.15 [0.14–0.15]|0.85 [0.81–0.87]|909.56|89.375|
|Northamptonshire|20212231|1812|0.13 [0.12–0.14]|0.77 [0.74–0.78]|255.08|76.25|
|Nottingham And Nottinghamshire|30578332|3469|0.13 [0.13–0.13]|0.77 [0.72–0.81]|419.5|141.25|
|Shropshire Telford And Wrekin|12789830|1503|0.18 [0.13–0.19]|0.68 [0.65–0.73]|277.1|82.5|
|Somerset|14537248|1982|0.1 [0.1–0.11]|0.7 [0.69–0.71]|220.78|69.375|
|South East London|50630135|5967|0.15 [0.14–0.17]|0.67 [0.58–0.71]|1019.69|86.875|
|South West London|42414639|3764|0.12 [0.09–0.14]|0.7 [0.63–0.74]|375.84|66.875|
|South Yorkshire|36464560|4265|0.1 [0.09–0.12]|0.85 [0.84–0.85]|601.64|138.125|
|Staffordshire And Stoke-On-Trent|28793463|2162|0.2 [0.2–0.21]|0.76 [0.7–0.81]|326.1|56.875|
|Suffolk And North East Essex|25729012|3458|0.12 [0.12–0.16]|0.81 [0.8–0.82]|496.780025|169.375|
|Surrey Heartlands|27449264|2612|0.1 [0.1–0.11]|0.61 [0.57–0.67]|348.74|23.125|
|Sussex|44413100|4588|0.13 [0.13–0.15]|0.7 [0.66–0.75]|753.04|86.875|
|West Yorkshire|64453325|6558|0.12 [0.12–0.13]|0.63 [0.6–0.68]|1118.84|181.25|

Table 1 Shows baseline characteristics for each ICB. Data has been summarised over the entire analysis period from July 2023 to June 2025

**Pricing**

Using the indicative cost data, we estimated a potential cost saving of £384 per treatment episode when switching from alteplase to tenecteplase. In the 12 months after the NICE guidance update in July 2024, total NHS expenditure was £13,530,205 on alteplase and £4,427,434 on tenecteplase. If all doses had been switched to tenecteplase after the NICE guidance update, the NHS could have saved approximately £3,064,858 during this 12 month period. Calculated cost per DDD for each ICB also varied with a mean of £1233 for alteplase (SD = £512) and a mean of £782 for tenecteplase (SD = £196).

**Discussion**

This analysis utilising OpenPrescribing Hospitals demonstrates a clear national shift from alteplase to tenecteplase following updated NICE guidance, but with substantial variation in adoption across ICBs in England. The most striking regional pattern was a consistent lag across all five London ICBs, which contrasts sharply with the national trend and rapid adoption of tenecteplase in many other ICBs. Baseline stroke care quality metrics, such as thrombolysis rate and the proportion of patients spending 90% of their admission on a stroke unit, showed no correlation with the speed or completeness of tenecteplase adoption.

From an economic perspective, this variability carries major implications. Tenecteplase offers a per-treatment saving of approximately £400 compared to alteplase. During the study period, NHS hospitals spent £13.5 million on alteplase and £4.4 million on tenecteplase; had all alteplase treatments been replaced with tenecteplase after the NICE guidance update, the NHS could have saved an estimated £3 million which is enough to fund 3,919 additional treatments with tenecteplase based on our average cost per DDD calculations. It is important to note, however, that this calculation is an estimate based upon indicative cost data and is not completely representative of formulary prices. These totals also only account for drug prices and not savings in specialist nursing time within the stroke unit, as tenecteplase is administered via a single bolus and does not require setting up and maintaining an infusion. The observed slow and inconsistent adoption therefore represents not only a missed opportunity for clinical standardisation but also a measurable economic inefficiency.

The ICBs showing the largest reductions in alteplase use and the highest increases in tenecteplase uptake included Mid and South Essex, Shropshire Telford and Wrekin, Dorset, Lancashire and South Cumbria, and Norfolk and Waveney, which appear to have undertaken near-complete formulary transitions. One plausible factor is adherence to the BIASP recommendation12 to replace alteplase entirely to minimise prescribing errors. The coexistence of both agents can create risk through look-alike/sound-alike confusion and dosing protocols. It is therefore possible that regions which fully transitioned achieved not only financial but also potential safety benefits, though the present study did not directly measure error rates.

The size of an ICB does not appear to be a dominant determinant of adoption speed. While several smaller systems transitioned rapidly, so too did some of the largest including North East and North Cumbria and Greater Manchester, suggesting that local governance structures, rather than scale, are key. Differences in how quickly ICBs operationalised NICE guidance may reflect internal leadership engagement, procurement efficiency, or regional formulary alignment processes.

The lack of correlation between stroke unit performance and thrombolytic adoption suggests that organisational determinants of infrastructure and pharmaceutical change are distinct. However, alternative explanations warrant consideration. Stroke unit metrics may largely reflect historical investment rather than present capacity to implement new clinical practices. Pharmacy and formulary decisions are often made at ICB or network level, decoupled from day-to-day clinical service delivery. Moreover, regional financial pressures could influence drug procurement independently of care quality metrics. These interpretations remain speculative, underscoring the need for qualitative and organisational-level data to clarify causal mechanisms.

London’s uniformly slow adoption remains the most striking and unexplained pattern. The capital’s ICBs combine high patient volumes, complex referral pathways and strong academic involvement, yet this appears to correlate with organisational inertia rather than leadership in implementation. One possibility is that the scale and complexity of tertiary stroke networks alongside layered governance delayed formulary changes. Further investigation through expert consultation or targeted interviews with regional stroke leads would help elucidate these barriers.

**Limitations**

Several limitations should be acknowledged when interpreting these findings. First, this analysis is based on aggregated pharmacy stock control data, meaning it cannot link changes in thrombolytic use to patient-level outcomes such as treatment times, functional recovery, or adverse events. Furthermore, the use of GP-registered population as the denominator introduces potential bias, as it does not directly reflect the number of stroke admissions within each ICB. Future analyses could adjust prescribing volume by stroke incidence using Hospital Episode Statistics (HES) data.

The interrupted time series approach assumes that no other concurrent interventions or contextual factors influenced thrombolytic prescribing during the study period. In reality, local formulary decisions, staffing changes, or supply chain issues could have contributed to observed trends. The analysis operates at the ICB level, raising the risk of ecological fallacy: variation between individual hospitals or clinicians within each ICB may be obscured, and findings cannot be inferred to reflect behaviours at the trust or prescriber level. Finally, the 12-month post-implementation observation period may not fully capture the longer-term adoption trajectory, as policy uptake and procurement processes often evolve over several years.

Another key limitation is within the calculation of pricing estimates for drug costs of alteplase and tenecteplase. The SCMD data includes indicative cost which is based on community pharmacy reimbursement prices and does not reflect the actual cost paid by hospitals as each hospital can have different true purchasing prices. To examine this, we examined the cost per DDD for each ICB and they fit within a bounded range with some outliers (see figure 8), which allowed us to make certain claims that using tenecteplase is cheaper. However, confidential price agreements can be different, and formal analysis requires access to actual cost information which we did not have.

**Conclusion**

This analysis demonstrates substantial regional heterogeneity in the adoption of tenecteplase following NICE guidance, revealing that implementation capability varies independently of established measures of stroke care quality. The lack of correlation between adoption speed, thrombolysis ratios and stroke unit performance suggests that operational agility depends on distinct organisational, financial and governance factors. London’s consistently slow adoption across all five ICBs highlights region-specific barriers, likely related to complex multi-trust governance and coordination within densely centralised hyperacute stroke networks.

Clinically and economically, this variation carries important implications. Full national replacement of alteplase with tenecteplase could have saved approximately £3 million in 12 months while simultaneously reducing nursing workload through simplified, single-bolus administration. Beyond cost efficiency, tenecteplase offers practical advantages for “drip-and-ship” stroke pathways, facilitating earlier treatment at district general hospitals before transfer to hyperacute centres and potentially improving equity of access to timely reperfusion therapy.

Further implementation research is needed to identify barriers to adoption, particularly within large metropolitan regions and to understand how organisational structures influence formulary change. OpenPrescribing dashboards could play a pivotal role in this next phase, providing transparent, near-real-time monitoring of thrombolytic prescribing across hospitals. Such tools would enable commissioners and clinicians to benchmark progress, identify lagging regions, and align economic and clinical priorities in the ongoing optimisation of national stroke care.

**Appendix**

**Formulary prices**

The current differences in national formulary prices are as follows:

Alteplase:

- 10mg powder and solvent for solution for injection vials: £172.80

- 20mg powder and solvent for solution for injection vials: £259.20

- 50mg powder and solvent for solution for infusion vials: £432.00

Tenecteplase:

- 5,000 unit (25mg) powder for solution for injection vials: £602.70

- 10,000 unit (50mg) powder and solvent for solution for injection vials: £602.70

Source for this is latest BNF data. 13 14

**Description of the secondary care medicines dataset**

The SCMD structure includes:

- YEAR_MONTH: Month

- ODS_CODE: Organisation Data Service code for each trust

- VMP_PRODUCT_NAME: Virtual Medicinal Product name

- TOTAL_QUANTITY_IN_VMP_UNIT: Volume prescribed

- INDICATIVE_COST: indicative cost based on reimbursement prices for medicines, does not reflect actual cost information

**Time series model specification**

Y_t = β₀ + β₁_time_t + β₂_intervention_t + β₃*.time_after_intervention_t + ε_t

Where:

- Y_t = outcome at time t (DDD of thrombolytic)

- time_t = time since study start

- intervention_t = binary indicator (0 before July 2024, 1 after)

- time_after_intervention_t = time since intervention

- β₂ = immediate level change

- β₃ = change in slope post-intervention

- ε_t = random noise

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%202.png>)

Figure 3 Changes in prescribing trends of Alteplase for each ICB categorised into three significance categories.

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%203.png>)

Figure 4 Changes in prescribing trends of tenecteplase for each ICB categorised into three significance categories

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%204.png>)

Figure 5 Total number of stroke patients admitted to ICBs according to SSNAP data

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%205.png>)

Figure 6 Thrombolysis ratios for each ICBs according to SSNAP data

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%206.png>)

Figure 7 Ratios of patients that spent 90% of their stay in stroke units according to SSNAP data

![tenecteplase](<6-Main-Notes/7-Attachments/tenecteplase%207.png>)

Figure 8 ICB level variation in price per dose of alteplase (blue) and tenecteplase (red)

|   |   |   |   |   |
|---|---|---|---|---|
|ICB Name|Intercept|Pre-intervention slope|Immediate level change (July 2024)|Post-intervention slope|
|LANCASHIRE AND SOUTH CUMBRIA|β = 0.2085 p = 2.03e-18 95% CI [0.1954–0.2217]|β = 0.0013 p = 1.28e-01 95% CI [-3e-04–0.0029]|β = 0.1164 p = 1.82e-05 95% CI [0.0756–0.1573]|β = -0.0228 p = 4.26e-09 95% CI [-0.0274–-0.0183]|
|SOUTH YORKSHIRE|β = 0.1704 p = 6.87e-09 95% CI [0.1354–0.2054]|β = 0.0019 p = 3.71e-01 95% CI [-0.0022–0.0059]|β = 0.0233 p = 2.90e-01 95% CI [-0.0187–0.0654]|β = -0.0125 p = 4.54e-04 95% CI [-0.0183–-0.0066]|
|HEREFORDSHIRE AND WORCESTERSHIRE|β = 0.163 p = 3.90e-07 95% CI [0.1198–0.2063]|β = 1e-04 p = 9.62e-01 95% CI [-0.005–0.0053]|β = 0.0274 p = 3.07e-01 95% CI [-0.0238–0.0785]|β = -0.0081 p = 1.59e-02 95% CI [-0.0142–-0.0021]|
|MID AND SOUTH ESSEX|β = 0.3541 p = 1.58e-10 95% CI [0.2957–0.4124]|β = -0.0021 p = 5.29e-01 95% CI [-0.0084–0.0042]|β = 0.1192 p = 1.56e-03 95% CI [0.0553–0.183]|β = -0.0336 p = 2.54e-05 95% CI [-0.0457–-0.0215]|
|BEDFORDSHIRE LUTON AND MILTON KEYNES|β = 0.2284 p = 3.05e-08 95% CI [0.177–0.2798]|β = -9e-04 p = 7.80e-01 95% CI [-0.007–0.0052]|β = 0.0279 p = 4.17e-01 95% CI [-0.0381–0.0939]|β = -0.0131 p = 2.73e-03 95% CI [-0.0206–-0.0056]|
|BIRMINGHAM AND SOLIHULL|β = 0.147 p = 1.93e-07 95% CI [0.1098–0.1842]|β = 2e-04 p = 9.49e-01 95% CI [-0.0054–0.0058]|β = 0.0846 p = 1.25e-03 95% CI [0.0404–0.1287]|β = -0.009 p = 3.83e-02 95% CI [-0.017–-0.0011]|
|NORTH EAST AND NORTH CUMBRIA|β = 0.2572 p = 1.01e-14 95% CI [0.2321–0.2823]|β = -6e-04 p = 6.28e-01 95% CI [-0.0032–0.0019]|β = 0.0623 p = 9.47e-05 95% CI [0.0372–0.0874]|β = -0.0196 p = 9.52e-08 95% CI [-0.0244–-0.0149]|
|DERBY AND DERBYSHIRE|β = 0.1808 p = 6.55e-09 95% CI [0.1438–0.2178]|β = -0.0025 p = 4.54e-01 95% CI [-0.0088–0.0039]|β = 0.0538 p = 5.35e-02 95% CI [0.0024–0.1051]|β = -0.0115 p = 3.32e-02 95% CI [-0.0213–-0.0016]|
|SUFFOLK AND NORTH EAST ESSEX|β = 0.2551 p = 8.36e-06 95% CI [0.1709–0.3394]|β = -9e-04 p = 8.49e-01 95% CI [-0.0105–0.0086]|β = 0.0198 p = 4.89e-01 95% CI [-0.0352–0.0749]|β = -0.0184 p = 5.76e-03 95% CI [-0.0301–-0.0067]|
|DEVON|β = 0.2159 p = 3.68e-15 95% CI [0.1959–0.2359]|β = -0.0041 p = 3.93e-03 95% CI [-0.0066–-0.0016]|β = 0.056 p = 5.57e-02 95% CI [0.002–0.11]|β = 0.0049 p = 1.57e-01 95% CI [-0.0016–0.0115]|
|LINCOLNSHIRE|β = 0.0864 p = 1.26e-02 95% CI [0.0246–0.1481]|β = 0.0052 p = 2.60e-01 95% CI [-0.0036–0.0139]|β = 0.0328 p = 3.40e-01 95% CI [-0.033–0.0986]|β = -0.0174 p = 2.85e-03 95% CI [-0.0274–-0.0074]|
|LEICESTER LEICESTERSHIRE AND RUTLAND|β = 0.2191 p = 4.39e-14 95% CI [0.196–0.2423]|β = -0.0092 p = 2.41e-04 95% CI [-0.0132–-0.0052]|β = 0.0747 p = 8.33e-03 95% CI [0.0247–0.1247]|β = 0.0013 p = 7.00e-01 95% CI [-0.0053–0.008]|
|SOUTH EAST LONDON|β = 0.1734 p = 3.80e-09 95% CI [0.139–0.2078]|β = 0.0066 p = 6.30e-02 95% CI [0–0.0131]|β = -0.0574 p = 1.15e-01 95% CI [-0.1257–0.0109]|β = -0.0078 p = 1.24e-01 95% CI [-0.0174–0.0017]|
|KENT AND MEDWAY|β = 0.1823 p = 2.84e-12 95% CI [0.1583–0.2064]|β = 0.0012 p = 4.84e-01 95% CI [-0.0021–0.0044]|β = 0.0525 p = 2.98e-02 95% CI [0.0085–0.0964]|β = -0.0191 p = 2.83e-05 95% CI [-0.0261–-0.0122]|
|HERTFORDSHIRE AND WEST ESSEX|β = 0.1069 p = 5.63e-07 95% CI [0.0778–0.136]|β = 0.0036 p = 9.81e-02 95% CI [-5e-04–0.0076]|β = -0.0194 p = 1.93e-01 95% CI [-0.0477–0.0088]|β = -0.0067 p = 7.78e-03 95% CI [-0.0111–-0.0023]|
|NORTH EAST LONDON|β = 0.1132 p = 3.91e-17 95% CI [0.1049–0.1215]|β = 0.0044 p = 1.62e-06 95% CI [0.0031–0.0057]|β = 0.0164 p = 4.55e-02 95% CI [0.0013–0.0314]|β = -0.013 p = 3.25e-14 95% CI [-0.0143–-0.0116]|
|NORTH CENTRAL LONDON|β = 0.1968 p = 9.90e-12 95% CI [0.169–0.2245]|β = -0.002 p = 3.99e-01 95% CI [-0.0065–0.0025]|β = -0.0202 p = 3.25e-01 95% CI [-0.0594–0.019]|β = 0.0049 p = 8.28e-02 95% CI [-4e-04–0.0102]|
|NORFOLK AND WAVENEY|β = 0.2875 p = 1.63e-13 95% CI [0.255–0.32]|β = -0.0033 p = 1.02e-01 95% CI [-0.0071–5e-04]|β = 0.1405 p = 6.13e-03 95% CI [0.0506–0.2304]|β = -0.0226 p = 5.06e-05 95% CI [-0.0312–-0.014]|
|STAFFORDSHIRE AND STOKE-ON-TRENT|β = 0.1117 p = 1.83e-09 95% CI [0.0905–0.1329]|β = 0.0032 p = 1.30e-02 95% CI [9e-04–0.0055]|β = 0.0287 p = 1.11e-01 95% CI [-0.0051–0.0625]|β = -0.0162 p = 1.36e-07 95% CI [-0.0203–-0.0122]|
|FRIMLEY|β = 0.0359 p = 1.93e-05 95% CI [0.0232–0.0485]|β = -1e-04 p = 9.18e-01 95% CI [-0.0018–0.0016]|β = -0.0212 p = 3.35e-01 95% CI [-0.0634–0.0209]|β = 0.0034 p = 2.49e-01 95% CI [-0.0022–0.0089]|
|SUSSEX|β = 0.2022 p = 1.16e-12 95% CI [0.1768–0.2276]|β = -0.0024 p = 3.51e-01 95% CI [-0.0072–0.0025]|β = 0.0709 p = 4.96e-03 95% CI [0.0269–0.1149]|β = -0.0118 p = 5.04e-04 95% CI [-0.0174–-0.0062]|
|SHROPSHIRE TELFORD AND WREKIN|β = 0.1907 p = 8.67e-04 95% CI [0.0951–0.2863]|β = 0.0053 p = 3.46e-01 95% CI [-0.0054–0.016]|β = 0.1059 p = 3.78e-02 95% CI [0.0126–0.1993]|β = -0.0286 p = 3.10e-03 95% CI [-0.0453–-0.0119]|
|GREATER MANCHESTER|β = 0.2231 p = 1.53e-10 95% CI [0.1864–0.2598]|β = 9e-04 p = 7.06e-01 95% CI [-0.0039–0.0057]|β = -0.0112 p = 4.62e-01 95% CI [-0.0404–0.018]|β = -0.0016 p = 6.00e-01 95% CI [-0.0077–0.0044]|
|HUMBER AND NORTH YORKSHIRE|β = 0.2303 p = 8.38e-10 95% CI [0.1885–0.272]|β = 0.0011 p = 6.99e-01 95% CI [-0.0042–0.0063]|β = 0.0377 p = 1.73e-01 95% CI [-0.0146–0.0901]|β = -0.0111 p = 3.87e-02 95% CI [-0.0209–-0.0013]|
|BATH AND NORTH EAST SOMERSET SWINDON AND WILTSHIRE|β = 0.2164 p = 2.49e-16 95% CI [0.1989–0.2338]|β = -0.002 p = 2.26e-01 95% CI [-0.005–0.0011]|β = 0.0349 p = 1.55e-01 95% CI [-0.0114–0.0811]|β = -0.0118 p = 7.38e-04 95% CI [-0.0177–-0.006]|
|NORTHAMPTONSHIRE|β = 0.1625 p = 1.35e-05 95% CI [0.1068–0.2182]|β = -0.0012 p = 7.62e-01 95% CI [-0.0091–0.0067]|β = 0.0319 p = 3.92e-01 95% CI [-0.0396–0.1034]|β = -0.0112 p = 7.13e-02 95% CI [-0.0228–3e-04]|
|GLOUCESTERSHIRE|β = 0.1903 p = 1.67e-07 95% CI [0.1426–0.2381]|β = -0.0048 p = 1.88e-01 95% CI [-0.0116–0.0021]|β = 0.0654 p = 1.33e-02 95% CI [0.0182–0.1126]|β = -0.0131 p = 3.42e-02 95% CI [-0.0243–-0.0018]|
|HAMPSHIRE AND ISLE OF WIGHT|β = 0.1618 p = 2.39e-12 95% CI [0.1407–0.1829]|β = 0.0081 p = 5.25e-04 95% CI [0.0043–0.012]|β = -0.0576 p = 1.67e-03 95% CI [-0.0887–-0.0265]|β = -0.0175 p = 1.76e-08 95% CI [-0.0214–-0.0137]|
|NORTH WEST LONDON|β = 0.1452 p = 1.72e-05 95% CI [0.0944–0.1959]|β = -1e-04 p = 9.78e-01 95% CI [-0.0059–0.0058]|β = -0.0217 p = 3.12e-01 95% CI [-0.0626–0.0193]|β = -6e-04 p = 8.57e-01 95% CI [-0.0072–0.006]|
|SOMERSET|β = 0.1198 p = 7.22e-05 95% CI [0.0726–0.1669]|β = 0.0059 p = 6.47e-02 95% CI [0–0.0119]|β = 0.0033 p = 8.85e-01 95% CI [-0.0415–0.0482]|β = -0.0135 p = 1.06e-02 95% CI [-0.0229–-0.0041]|
|NOTTINGHAM AND NOTTINGHAMSHIRE|β = 0.1672 p = 1.21e-07 95% CI [0.1261–0.2083]|β = 0.0019 p = 4.52e-01 95% CI [-0.0029–0.0066]|β = -0.0583 p = 6.23e-03 95% CI [-0.0956–-0.0209]|β = -0.0073 p = 5.30e-02 95% CI [-0.0143–-3e-04]|
|CORNWALL AND THE ISLES OF SCILLY|β = 0.1141 p = 8.01e-04 95% CI [0.0574–0.1708]|β = 0.0018 p = 6.16e-01 95% CI [-0.0052–0.0089]|β = -0.019 p = 5.91e-01 95% CI [-0.0874–0.0493]|β = -0.0053 p = 2.59e-01 95% CI [-0.0141–0.0036]|
|BUCKINGHAMSHIRE OXFORDSHIRE AND BERKSHIRE WEST|β = 0.2466 p = 3.16e-12 95% CI [0.2139–0.2793]|β = 0.002 p = 4.01e-01 95% CI [-0.0026–0.0066]|β = -0.0164 p = 4.40e-01 95% CI [-0.057–0.0243]|β = -0.019 p = 1.38e-05 95% CI [-0.0256–-0.0125]|
|BLACK COUNTRY|β = 0.1414 p = 1.91e-08 95% CI [0.1105–0.1723]|β = 0.0053 p = 1.05e-02 95% CI [0.0016–0.009]|β = 0.0075 p = 7.33e-01 95% CI [-0.0351–0.0501]|β = -0.0187 p = 3.38e-06 95% CI [-0.0244–-0.0129]|
|CAMBRIDGESHIRE AND PETERBOROUGH|β = 0.2943 p = 2.77e-12 95% CI [0.2555–0.333]|β = -0.0048 p = 7.27e-02 95% CI [-0.0097–2e-04]|β = 0.0445 p = 3.73e-01 95% CI [-0.0511–0.1401]|β = -0.0098 p = 6.97e-02 95% CI [-0.0199–2e-04]|
|BRISTOL NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE|β = 0.1138 p = 6.86e-08 95% CI [0.0869–0.1408]|β = 0.0022 p = 4.10e-01 95% CI [-0.0029–0.0073]|β = 0.0505 p = 2.15e-02 95% CI [0.0108–0.0901]|β = -0.0096 p = 2.11e-02 95% CI [-0.0171–-0.0021]|
|DORSET|β = 0.1518 p = 2.35e-10 95% CI [0.1262–0.1773]|β = 0.0066 p = 2.45e-03 95% CI [0.0029–0.0103]|β = 0.0651 p = 8.91e-02 95% CI [-0.0063–0.1364]|β = -0.0256 p = 2.04e-05 95% CI [-0.0346–-0.0165]|
|SOUTH WEST LONDON|β = 0.0951 p = 1.05e-05 95% CI [0.0632–0.1271]|β = 0.0027 p = 2.74e-01 95% CI [-0.002–0.0073]|β = -0.0556 p = 8.82e-03 95% CI [-0.0931–-0.018]|β = -0.0037 p = 1.31e-01 95% CI [-0.0083–9e-04]|
|WEST YORKSHIRE|β = 0.1544 p = 2.20e-09 95% CI [0.1248–0.1841]|β = 0.0047 p = 1.79e-02 95% CI [0.0011–0.0083]|β = 0.0145 p = 5.05e-01 95% CI [-0.0274–0.0564]|β = -0.0145 p = 7.74e-07 95% CI [-0.0185–-0.0104]|
|COVENTRY AND WARWICKSHIRE|β = 0.181 p = 1.44e-05 95% CI [0.1186–0.2433]|β = -7e-04 p = 8.51e-01 95% CI [-0.0082–0.0068]|β = 0.067 p = 1.79e-01 95% CI [-0.0274–0.1614]|β = -0.0084 p = 3.88e-01 95% CI [-0.0272–0.0103]|
|SURREY HEARTLANDS|β = 0.1256 p = 4.28e-12 95% CI [0.1087–0.1425]|β = 0.0011 p = 3.04e-01 95% CI [-0.001–0.0032]|β = 0.0019 p = 7.70e-01 95% CI [-0.0108–0.0146]|β = -0.0041 p = 2.83e-03 95% CI [-0.0065–-0.0017]|
|CHESHIRE AND MERSEYSIDE|β = 0.2157 p = 1.15e-14 95% CI [0.1945–0.2369]|β = -2e-04 p = 8.69e-01 95% CI [-0.0026–0.0022]|β = 0.0279 p = 3.87e-01 95% CI [-0.034–0.0899]|β = -0.0103 p = 9.93e-03 95% CI [-0.0173–-0.0032]|

Table 2 ITSA results for alteplase data

|   |   |   |   |   |
|---|---|---|---|---|
|ICB Name|Intercept|Pre-intervention slope|Immediate level change (July 2024)|Post-intervention slope|
|LANCASHIRE AND SOUTH CUMBRIA|β = 0.0066 p = 3.45e-01 95% CI [-0.0068–0.02]|β = -2e-04 p = 8.53e-01 95% CI [-0.0017–0.0014]|β = -0.0645 p = 7.25e-03 95% CI [-0.1068–-0.0222]|β = 0.0233 p = 6.36e-09 95% CI [0.0185–0.0281]|
|SOUTH YORKSHIRE|β = -0.0014 p = 2.10e-01 95% CI [-0.0034–7e-04]|β = 3e-04 p = 1.43e-01 95% CI [-1e-04–7e-04]|β = -0.024 p = 2.15e-01 95% CI [-0.0607–0.0127]|β = 0.0145 p = 1.42e-06 95% CI [0.0103–0.0187]|
|HEREFORDSHIRE AND WORCESTERSHIRE|β = 0.0062 p = 2.00e-01 95% CI [-0.003–0.0153]|β = -4e-04 p = 4.74e-01 95% CI [-0.0014–6e-04]|β = 0.0742 p = 2.54e-02 95% CI [0.014–0.1345]|β = 0.0093 p = 1.82e-02 95% CI [0.0022–0.0163]|
|MID AND SOUTH ESSEX|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = -0.0251 p = 6.09e-01 95% CI [-0.1196–0.0695]|β = 0.026 p = 2.18e-04 95% CI [0.0147–0.0373]|
|BEDFORDSHIRE LUTON AND MILTON KEYNES|β = -0.0044 p = 5.27e-01 95% CI [-0.0178–0.009]|β = 0.0015 p = 1.91e-01 95% CI [-7e-04–0.0037]|β = -0.0292 p = 3.57e-02 95% CI [-0.0547–-0.0038]|β = 0.0084 p = 2.44e-03 95% CI [0.0036–0.0131]|
|BIRMINGHAM AND SOLIHULL|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0.0242 p = 4.58e-02 95% CI [0.0019–0.0466]|β = 0.0029 p = 7.98e-02 95% CI [-2e-04–0.0059]|
|NORTH EAST AND NORTH CUMBRIA|β = 0.0035 p = 7.19e-02 95% CI [-1e-04–0.0071]|β = -3e-04 p = 1.87e-01 95% CI [-7e-04–1e-04]|β = 0.0124 p = 5.65e-01 95% CI [-0.0291–0.0538]|β = 0.0148 p = 1.44e-05 95% CI [0.0097–0.0199]|
|DERBY AND DERBYSHIRE|β = 0 p = NaN 95% CI [NaN–NaN]|β = 0 p = NaN 95% CI [NaN–NaN]|β = -0.0057 p = 6.64e-01 95% CI [-0.0309–0.0195]|β = 0.0095 p = 2.02e-03 95% CI [0.0043–0.0148]|
|SUFFOLK AND NORTH EAST ESSEX|β = -4e-04 p = 6.38e-01 95% CI [-0.0018–0.0011]|β = 2e-04 p = 2.66e-01 95% CI [-1e-04–6e-04]|β = 0.0339 p = 4.59e-01 95% CI [-0.0541–0.1219]|β = 0.0142 p = 1.61e-02 95% CI [0.0036–0.0249]|
|DEVON|β = 0.009 p = 1.61e-02 95% CI [0.0023–0.0157]|β = -9e-04 p = 2.54e-02 95% CI [-0.0016–-2e-04]|β = 0.0105 p = 4.05e-01 95% CI [-0.0137–0.0348]|β = 0.0032 p = 2.41e-02 95% CI [6e-04–0.0057]|
|LINCOLNSHIRE|β = 0.0142 p = 2.08e-01 95% CI [-0.0072–0.0355]|β = -8e-04 p = 5.23e-01 95% CI [-0.0033–0.0016]|β = -0.0215 p = 1.17e-01 95% CI [-0.0473–0.0042]|β = 0.0082 p = 3.84e-03 95% CI [0.0033–0.0131]|
|LEICESTER LEICESTERSHIRE AND RUTLAND|β = -7e-04 p = 8.19e-01 95% CI [-0.0069–0.0054]|β = 6e-04 p = 1.54e-01 95% CI [-2e-04–0.0015]|β = 0.0084 p = 7.54e-01 95% CI [-0.0433–0.06]|β = 0.0079 p = 7.47e-03 95% CI [0.0027–0.0132]|
|SOUTH EAST LONDON|β = 0.0055 p = 5.02e-01 95% CI [-0.0103–0.0214]|β = 1e-04 p = 9.57e-01 95% CI [-0.0023–0.0024]|β = -0.0232 p = 9.81e-02 95% CI [-0.0495–0.003]|β = 0.0069 p = 3.87e-02 95% CI [8e-04–0.013]|
|KENT AND MEDWAY|β = 0.0262 p = 2.15e-03 95% CI [0.0116–0.0408]|β = -0.0016 p = 7.65e-02 95% CI [-0.0033–1e-04]|β = 8e-04 p = 9.77e-01 95% CI [-0.0513–0.0528]|β = 0.0138 p = 3.85e-04 95% CI [0.0074–0.0202]|
|HERTFORDSHIRE AND WEST ESSEX|β = -2e-04 p = 8.72e-01 95% CI [-0.0029–0.0025]|β = 4e-04 p = 1.07e-01 95% CI [-1e-04–9e-04]|β = -0.0064 p = 3.73e-01 95% CI [-0.0201–0.0073]|β = 0.0045 p = 2.11e-03 95% CI [0.002–0.007]|
|NORTH EAST LONDON|β = 5e-04 p = 4.07e-01 95% CI [-7e-04–0.0018]|β = 0 p = 7.91e-01 95% CI [-1e-04–1e-04]|β = -0.0046 p = 7.41e-01 95% CI [-0.0317–0.0224]|β = 0.0096 p = 5.69e-05 95% CI [0.0059–0.0133]|
|NORTH CENTRAL LONDON|β = -0.0028 p = 4.36e-01 95% CI [-0.0098–0.0041]|β = 0.0012 p = 1.44e-01 95% CI [-4e-04–0.0028]|β = -0.0115 p = 9.96e-02 95% CI [-0.0246–0.0016]|β = -7e-04 p = 4.51e-01 95% CI [-0.0024–0.0011]|
|NORFOLK AND WAVENEY|β = 0.0073 p = 1.09e-01 95% CI [-0.0012–0.0158]|β = -2e-04 p = 6.28e-01 95% CI [-0.0012–7e-04]|β = -0.0454 p = 1.48e-02 95% CI [-0.0787–-0.012]|β = 0.0189 p = 1.10e-07 95% CI [0.0143–0.0235]|
|STAFFORDSHIRE AND STOKE-ON-TRENT|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = -0.0119 p = 3.00e-01 95% CI [-0.0338–0.01]|β = 0.0079 p = 8.41e-04 95% CI [0.0039–0.0118]|
|FRIMLEY|β = -0.0101 p = 6.29e-02 95% CI [-0.0201–0]|β = 0.0027 p = 1.91e-03 95% CI [0.0012–0.0042]|β = -0.0275 p = 2.16e-01 95% CI [-0.0697–0.0147]|β = 0.0116 p = 5.04e-04 95% CI [0.0061–0.017]|
|SUSSEX|β = 0 p = NaN 95% CI [NaN–NaN]|β = 0 p = NaN 95% CI [NaN–NaN]|β = -0.0508 p = 6.68e-02 95% CI [-0.1022–6e-04]|β = 0.0138 p = 3.47e-03 95% CI [0.0056–0.022]|
|SHROPSHIRE TELFORD AND WREKIN|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = -0.0603 p = 9.32e-02 95% CI [-0.1274–0.0067]|β = 0.029 p = 1.12e-04 95% CI [0.0171–0.0409]|
|GREATER MANCHESTER|β = 0.0054 p = 4.64e-03 95% CI [0.0021–0.0086]|β = -5e-04 p = 5.38e-02 95% CI [-9e-04–0]|β = 0.0143 p = 2.14e-01 95% CI [-0.0075–0.0361]|β = 0.0028 p = 4.29e-02 95% CI [3e-04–0.0054]|
|HUMBER AND NORTH YORKSHIRE|β = 0.0047 p = 6.37e-03 95% CI [0.0017–0.0078]|β = -5e-04 p = 2.04e-02 95% CI [-8e-04–-1e-04]|β = -0.0226 p = 6.64e-04 95% CI [-0.0335–-0.0116]|β = 0.0134 p = 2.43e-15 95% CI [0.0122–0.0146]|
|BATH AND NORTH EAST SOMERSET SWINDON AND WILTSHIRE|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = -0.0176 p = 3.47e-01 95% CI [-0.0533–0.0182]|β = 0.0158 p = 9.67e-06 95% CI [0.0105–0.0211]|
|NORTHAMPTONSHIRE|β = 0 p = NaN 95% CI [NaN–NaN]|β = 0 p = NaN 95% CI [NaN–NaN]|β = -0.0097 p = 6.27e-01 95% CI [-0.0483–0.0289]|β = 0.013 p = 3.44e-05 95% CI [0.0082–0.0178]|
|GLOUCESTERSHIRE|β = 0 p = NaN 95% CI [NaN–NaN]|β = 0 p = NaN 95% CI [NaN–NaN]|β = 0.0118 p = 5.36e-01 95% CI [-0.0248–0.0483]|β = 0.0094 p = 1.25e-03 95% CI [0.0045–0.0142]|
|HAMPSHIRE AND ISLE OF WIGHT|β = 0.0296 p = 1.02e-07 95% CI [0.0224–0.0367]|β = -3e-04 p = 6.01e-01 95% CI [-0.0014–8e-04]|β = 0.0708 p = 1.72e-01 95% CI [-0.0273–0.1688]|β = 0.0054 p = 3.42e-01 95% CI [-0.0054–0.0162]|
|NORTH WEST LONDON|β = 0.0015 p = 1.41e-01 95% CI [-4e-04–0.0033]|β = -2e-04 p = 1.43e-01 95% CI [-4e-04–0]|β = -0.0223 p = 7.06e-02 95% CI [-0.0452–6e-04]|β = 0.0076 p = 1.49e-03 95% CI [0.0035–0.0116]|
|SOMERSET|β = 0.0069 p = 1.41e-01 95% CI [-0.0019–0.0158]|β = -8e-04 p = 1.43e-01 95% CI [-0.0018–2e-04]|β = -0.0149 p = 4.89e-01 95% CI [-0.0565–0.0266]|β = 0.0179 p = 6.47e-04 95% CI [0.0092–0.0265]|
|NOTTINGHAM AND NOTTINGHAMSHIRE|β = -0.0016 p = 2.10e-01 95% CI [-0.0041–8e-04]|β = 4e-04 p = 1.43e-01 95% CI [-1e-04–9e-04]|β = 0.0361 p = 3.73e-01 95% CI [-0.0416–0.1139]|β = 0.0076 p = 8.45e-02 95% CI [-6e-04–0.0158]|
|CORNWALL AND THE ISLES OF SCILLY|β = 0.0142 p = 1.77e-01 95% CI [-0.0057–0.034]|β = -6e-04 p = 6.15e-01 95% CI [-0.0028–0.0017]|β = 0.0125 p = 6.75e-01 95% CI [-0.0452–0.0703]|β = 0.0047 p = 2.56e-01 95% CI [-0.0032–0.0126]|
|BUCKINGHAMSHIRE OXFORDSHIRE AND BERKSHIRE WEST|β = -0.0011 p = 7.39e-01 95% CI [-0.0077–0.0055]|β = 9e-04 p = 2.74e-01 95% CI [-7e-04–0.0025]|β = -0.0114 p = 6.01e-01 95% CI [-0.0536–0.0308]|β = 0.012 p = 5.91e-04 95% CI [0.0062–0.0178]|
|BLACK COUNTRY|β = 0.0075 p = 4.76e-02 95% CI [5e-04–0.0144]|β = -3e-04 p = 4.89e-01 95% CI [-0.0011–5e-04]|β = -0.0121 p = 1.53e-01 95% CI [-0.0281–0.0039]|β = 0.0122 p = 4.91e-08 95% CI [0.0094–0.015]|
|CAMBRIDGESHIRE AND PETERBOROUGH|β = -0.0235 p = 3.91e-02 95% CI [-0.0443–-0.0026]|β = 0.0081 p = 2.75e-06 95% CI [0.0056–0.0105]|β = 0.0157 p = 5.16e-01 95% CI [-0.0309–0.0622]|β = -0.0062 p = 3.90e-02 95% CI [-0.0117–-7e-04]|
|BRISTOL NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = -0.0229 p = 4.86e-02 95% CI [-0.0442–-0.0015]|β = 0.0089 p = 9.46e-05 95% CI [0.0053–0.0125]|
|DORSET|β = 0 p = 1.00e+00 95% CI [0–0]|β = 0 p = 1.00e+00 95% CI [0–0]|β = -0.0355 p = 1.20e-01 95% CI [-0.0783–0.0074]|β = 0.0235 p = 7.73e-09 95% CI [0.0186–0.0283]|
|SOUTH WEST LONDON|β = 0.0072 p = 3.41e-02 95% CI [0.001–0.0134]|β = -5e-04 p = 1.97e-01 95% CI [-0.0012–2e-04]|β = 0.0068 p = 6.58e-01 95% CI [-0.0228–0.0363]|β = 0.0034 p = 7.96e-02 95% CI [-2e-04–0.007]|
|WEST YORKSHIRE|β = 0.0071 p = 1.95e-01 95% CI [-0.0033–0.0175]|β = 0 p = 9.82e-01 95% CI [-0.0012–0.0012]|β = 4e-04 p = 9.73e-01 95% CI [-0.0247–0.0256]|β = 0.0064 p = 1.04e-04 95% CI [0.0038–0.009]|
|COVENTRY AND WARWICKSHIRE|β = 0.0089 p = 9.54e-03 95% CI [0.0028–0.015]|β = -9e-04 p = 1.55e-02 95% CI [-0.0016–-2e-04]|β = -0.0396 p = 1.07e-01 95% CI [-0.0856–0.0064]|β = 0.0139 p = 8.21e-03 95% CI [0.0046–0.0232]|
|SURREY HEARTLANDS|β = 0.0023 p = 4.07e-01 95% CI [-0.0031–0.0077]|β = -1e-04 p = 7.91e-01 95% CI [-6e-04–5e-04]|β = -0.0086 p = 3.30e-01 95% CI [-0.0254–0.0082]|β = 0.0035 p = 6.11e-02 95% CI [0–0.0069]|
|CHESHIRE AND MERSEYSIDE|β = 0.0113 p = 5.17e-03 95% CI [0.0042–0.0184]|β = 1e-04 p = 8.66e-01 95% CI [-0.0012–0.0014]|β = -0.0275 p = 7.75e-02 95% CI [-0.0565–0.0015]|β = 0.0128 p = 1.09e-06 95% CI [0.0091–0.0164]|

Table 3 ITSA results for tenecteplase data

**Ranking lists**

Alteplase slope change ranked

"MID AND SOUTH ESSEX"

"SHROPSHIRE, TELFORD AND WREKIN"

"DORSET"

"LANCASHIRE AND SOUTH CUMBRIA"

"NORFOLK AND WAVENEY"

"NORTH EAST AND NORTH CUMBRIA"

"KENT AND MEDWAY"

"BUCKINGHAMSHIRE, OXFORDSHIRE AND BERKSHIRE WEST"

"BLACK COUNTRY"

"SUFFOLK AND NORTH EAST ESSEX"

"HAMPSHIRE AND ISLE OF WIGHT"

"LINCOLNSHIRE"

"STAFFORDSHIRE AND STOKE-ON-TRENT"

"WEST YORKSHIRE"

"SOMERSET"

"BEDFORDSHIRE, LUTON AND MILTON KEYNES"

"GLOUCESTERSHIRE"

"NORTH EAST LONDON"

"SOUTH YORKSHIRE"

"BATH AND NORTH EAST SOMERSET, SWINDON AND WILTSHIRE"

"SUSSEX"

"DERBY AND DERBYSHIRE"

"NORTHAMPTONSHIRE"

"HUMBER AND NORTH YORKSHIRE"

"CHESHIRE AND MERSEYSIDE"

"CAMBRIDGESHIRE AND PETERBOROUGH"

"BRISTOL, NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE"

"BIRMINGHAM AND SOLIHULL"

"COVENTRY AND WARWICKSHIRE"

"HEREFORDSHIRE AND WORCESTERSHIRE"

"SOUTH EAST LONDON"

"NOTTINGHAM AND NOTTINGHAMSHIRE"

"HERTFORDSHIRE AND WEST ESSEX"

"CORNWALL AND THE ISLES OF SCILLY"

"DEVON"

"NORTH CENTRAL LONDON"

"SURREY HEARTLANDS"

"SOUTH WEST LONDON"

"FRIMLEY"

"GREATER MANCHESTER"

"LEICESTER, LEICESTERSHIRE AND RUTLAND"

"NORTH WEST LONDON"

Tenecteplase slope change ranked

"SHROPSHIRE, TELFORD AND WREKIN"

"MID AND SOUTH ESSEX"

"DORSET"

"LANCASHIRE AND SOUTH CUMBRIA"

"NORFOLK AND WAVENEY"

"SOMERSET"

"BATH AND NORTH EAST SOMERSET, SWINDON AND WILTSHIRE"

"NORTH EAST AND NORTH CUMBRIA"

"SOUTH YORKSHIRE"

"SUFFOLK AND NORTH EAST ESSEX"

"COVENTRY AND WARWICKSHIRE"

"SUSSEX"

"KENT AND MEDWAY"

"HUMBER AND NORTH YORKSHIRE"

"NORTHAMPTONSHIRE"

"CHESHIRE AND MERSEYSIDE"

"BLACK COUNTRY"

"BUCKINGHAMSHIRE, OXFORDSHIRE AND BERKSHIRE WEST"

"FRIMLEY"

"NORTH EAST LONDON"

"DERBY AND DERBYSHIRE"

"GLOUCESTERSHIRE"

"HEREFORDSHIRE AND WORCESTERSHIRE"

"BRISTOL, NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE"

"BEDFORDSHIRE, LUTON AND MILTON KEYNES"

"LINCOLNSHIRE"

"LEICESTER, LEICESTERSHIRE AND RUTLAND"

"STAFFORDSHIRE AND STOKE-ON-TRENT"

"NOTTINGHAM AND NOTTINGHAMSHIRE"

"NORTH WEST LONDON"

"SOUTH EAST LONDON"

"WEST YORKSHIRE"

"CAMBRIDGESHIRE AND PETERBOROUGH"

"HAMPSHIRE AND ISLE OF WIGHT"

"CORNWALL AND THE ISLES OF SCILLY"

"HERTFORDSHIRE AND WEST ESSEX"

"SURREY HEARTLANDS"

"SOUTH WEST LONDON"

"DEVON"

"BIRMINGHAM AND SOLIHULL"

"GREATER MANCHESTER"

"NORTH CENTRAL LONDON"

ICBs with the most patients

[1] "NORTH EAST AND NORTH CUMBRIA"

[2] "GREATER MANCHESTER"

[3] "CHESHIRE AND MERSEYSIDE"

[4] "NORTH WEST LONDON"

[5] "WEST YORKSHIRE"

[6] "HUMBER AND NORTH YORKSHIRE"

[7] "HAMPSHIRE AND ISLE OF WIGHT"

[8] "SOUTH EAST LONDON"

[9] "LANCASHIRE AND SOUTH CUMBRIA"

[10] "NORTH EAST LONDON"

[11] "BIRMINGHAM AND SOLIHULL"

[12] "DEVON"

[13] "KENT AND MEDWAY"

[14] "SUSSEX"

[15] "SOUTH YORKSHIRE"

[16] "BUCKINGHAMSHIRE, OXFORDSHIRE AND BERKSHIRE WEST"

[17] "SOUTH WEST LONDON"

[18] "MID AND SOUTH ESSEX"

[19] "DERBY AND DERBYSHIRE"

[20] "NORFOLK AND WAVENEY"

[21] "NOTTINGHAM AND NOTTINGHAMSHIRE"

[22] "SUFFOLK AND NORTH EAST ESSEX"

[23] "CAMBRIDGESHIRE AND PETERBOROUGH"

[24] "DORSET"

[25] "BLACK COUNTRY"

[26] "BATH AND NORTH EAST SOMERSET, SWINDON AND WILTSHIRE"

[27] "NORTH CENTRAL LONDON"

[28] "HERTFORDSHIRE AND WEST ESSEX"

[29] "BRISTOL, NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE"

[30] "SURREY HEARTLANDS"

[31] "HEREFORDSHIRE AND WORCESTERSHIRE"

[32] "LEICESTER, LEICESTERSHIRE AND RUTLAND"

[33] "BEDFORDSHIRE, LUTON AND MILTON KEYNES"

[34] "STAFFORDSHIRE AND STOKE-ON-TRENT"

[35] "COVENTRY AND WARWICKSHIRE"

[36] "SOMERSET"

[37] "NORTHAMPTONSHIRE"

[38] "LINCOLNSHIRE"

[39] "GLOUCESTERSHIRE"

[40] "CORNWALL AND THE ISLES OF SCILLY"

[41] "SHROPSHIRE, TELFORD AND WREKIN"

[42] "FRIMLEY"

Highest thrombolysis ratio

[1] "FRIMLEY"

[2] "BUCKINGHAMSHIRE, OXFORDSHIRE AND BERKSHIRE WEST"

[3] "STAFFORDSHIRE AND STOKE-ON-TRENT"

[4] "CAMBRIDGESHIRE AND PETERBOROUGH"

[5] "BEDFORDSHIRE, LUTON AND MILTON KEYNES"

[6] "HAMPSHIRE AND ISLE OF WIGHT"

[7] "MID AND SOUTH ESSEX"

[8] "SHROPSHIRE, TELFORD AND WREKIN"

[9] "NORTH EAST LONDON"

[10] "KENT AND MEDWAY"

[11] "HUMBER AND NORTH YORKSHIRE"

[12] "NORFOLK AND WAVENEY"

[13] "SOUTH EAST LONDON"

[14] "LEICESTER, LEICESTERSHIRE AND RUTLAND"

[15] "CHESHIRE AND MERSEYSIDE"

[16] "BRISTOL, NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE"

[17] "NORTH EAST AND NORTH CUMBRIA"

[18] "NORTH WEST LONDON"

[19] "SUSSEX"

[20] "LANCASHIRE AND SOUTH CUMBRIA"

[21] "COVENTRY AND WARWICKSHIRE"

[22] "SUFFOLK AND NORTH EAST ESSEX"

[23] "HERTFORDSHIRE AND WEST ESSEX"

[24] "NOTTINGHAM AND NOTTINGHAMSHIRE"

[25] "BLACK COUNTRY"

[26] "NORTHAMPTONSHIRE"

[27] "HEREFORDSHIRE AND WORCESTERSHIRE"

[28] "WEST YORKSHIRE"

[29] "DORSET"

[30] "NORTH CENTRAL LONDON"

[31] "GREATER MANCHESTER"

[32] "DEVON"

[33] "SOUTH WEST LONDON"

[34] "GLOUCESTERSHIRE"

[35] "SOUTH YORKSHIRE"

[36] "SURREY HEARTLANDS"

[37] "LINCOLNSHIRE"

[38] "SOMERSET"

[39] "BATH AND NORTH EAST SOMERSET, SWINDON AND WILTSHIRE"

[40] "BIRMINGHAM AND SOLIHULL"

[41] "DERBY AND DERBYSHIRE"

[42] "CORNWALL AND THE ISLES OF SCILLY"

Highest ninety percent stay in a stroke unit ratio

[1] "KENT AND MEDWAY"

[2] "HERTFORDSHIRE AND WEST ESSEX"

[3] "HAMPSHIRE AND ISLE OF WIGHT"

[4] "NORTH EAST AND NORTH CUMBRIA"

[5] "NORTH WEST LONDON"

[6] "SOUTH YORKSHIRE"

[7] "GLOUCESTERSHIRE"

[8] "BUCKINGHAMSHIRE, OXFORDSHIRE AND BERKSHIRE WEST"

[9] "COVENTRY AND WARWICKSHIRE"

[10] "GREATER MANCHESTER"

[11] "SUFFOLK AND NORTH EAST ESSEX"

[12] "FRIMLEY"

[13] "CHESHIRE AND MERSEYSIDE"

[14] "LANCASHIRE AND SOUTH CUMBRIA"

[15] "HUMBER AND NORTH YORKSHIRE"

[16] "BEDFORDSHIRE, LUTON AND MILTON KEYNES"

[17] "MID AND SOUTH ESSEX"

[18] "DEVON"

[19] "NORTH EAST LONDON"

[20] "LEICESTER, LEICESTERSHIRE AND RUTLAND"

[21] "BATH AND NORTH EAST SOMERSET, SWINDON AND WILTSHIRE"

[22] "NORTHAMPTONSHIRE"

[23] "BRISTOL, NORTH SOMERSET AND SOUTH GLOUCESTERSHIRE"

[24] "HEREFORDSHIRE AND WORCESTERSHIRE"

[25] "STAFFORDSHIRE AND STOKE-ON-TRENT"

[26] "CORNWALL AND THE ISLES OF SCILLY"

[27] "NOTTINGHAM AND NOTTINGHAMSHIRE"

[28] "NORFOLK AND WAVENEY"

[29] "DERBY AND DERBYSHIRE"

[30] "SOMERSET"

[31] "BIRMINGHAM AND SOLIHULL"

[32] "SUSSEX"

[33] "NORTH CENTRAL LONDON"

[34] "BLACK COUNTRY"

[35] "SHROPSHIRE, TELFORD AND WREKIN"

[36] "SOUTH WEST LONDON"

[37] "DORSET"

[38] "WEST YORKSHIRE"

[39] "SOUTH EAST LONDON"

[40] "CAMBRIDGESHIRE AND PETERBOROUGH"

[41] "SURREY HEARTLANDS"

[42] "LINCOLNSHIRE"

Bibliography

1. Granger, C. B., Califf, R. M. & Topol, E. J. Thrombolytic Therapy for Acute Myocardial Infarction. _Drugs_ **44**, 293–325 (1992).

2. Arcasoy, S. M. & Kreit, J. W. Thrombolytic Therapy of Pulmonary Embolism: A Comprehensive Review of Current Evidence. _Chest_ **115**, 1695–1707 (1999).

3. Wardlaw, J. M., Murray, V., Berge, E. & Zoppo, G. J. del. Thrombolysis for acute ischaemic stroke. _Cochrane Database of Systematic Reviews_ https://doi.org/10.1002/14651858.CD000213.pub3 (2014) doi:10.1002/14651858.CD000213.pub3.

4. Zijlstra, F. _et al._ Long-Term Benefit of Primary Angioplasty as Compared with Thrombolytic Therapy for Acute Myocardial Infarction. _New England Journal of Medicine_ **341**, 1413–1419 (1999).

5. Konstantinides, S. V. _et al._ 2019 ESC Guidelines for the diagnosis and management of acute pulmonary embolism developed in collaboration with the European Respiratory Society (ERS): The Task Force for the diagnosis and management of acute pulmonary embolism of the European Society of Cardiology (ESC). _Eur Heart J_ **41**, 543–603 (2020).

6. SSNAP - National. https://www.strokeaudit.org/Results2/Clinical-audit/National-Results.aspx.

7. Xiong, Y. _et al._ Tenecteplase for Ischemic Stroke at 4.5 to 24 Hours without Thrombectomy. _New England Journal of Medicine_ **391**, 203–212 (2024).

8. Muir, K. W. _et al._ Tenecteplase versus alteplase for acute stroke within 4·5 h of onset (ATTEST-2): a randomised, parallel group, open-label trial. _The Lancet Neurology_ **23**, 1087–1096 (2024).

9. Roaldsen, M. B. _et al._ Safety and efficacy of tenecteplase in patients with wake-up stroke assessed by non-contrast CT (TWIST): a multicentre, open-label, randomised controlled trial. _The Lancet Neurology_ **22**, 117–126 (2023).

10. Menon, B. K. _et al._ Intravenous tenecteplase compared with alteplase for acute ischaemic stroke in Canada (AcT): a pragmatic, multicentre, open-label, registry-linked, randomised, controlled, non-inferiority trial. _The Lancet_ **400**, 161–169 (2022).

11. Campbell, B. C. V. _et al._ Tenecteplase versus Alteplase before Thrombectomy for Ischemic Stroke. _New England Journal of Medicine_ **378**, 1573–1582 (2018).

12. Stacy. BIASP Consensus Document - Tenecteplase. _BIASP - The British Irish Association of Stroke Physicians_ https://biasp.org/biasp-consensus-document-tenecteplase/ (2025).

13. Medicinal forms | Alteplase | Drugs | BNF content published by NICE. https://bnf.nice.org.uk/drugs/alteplase/medicinal-forms/.

14. Medicinal forms | Tenecteplase | Drugs | BNF content published by NICE. https://bnf.nice.org.uk/drugs/tenecteplase/medicinal-forms/.