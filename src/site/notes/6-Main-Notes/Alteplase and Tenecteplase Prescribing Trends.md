---
{"dg-publish":true,"permalink":"/6-main-notes/alteplase-and-tenecteplase-prescribing-trends/","noteIcon":""}
---

### Understanding Variation in Thrombolytic Prescribing Patterns Between Integrated Care Boards: A Time Series Analysis

#### Description

This report examines the key motivations for investigating tenecteplase and alteplase prescribing variation, provides comprehensive analysis of prescribing patterns following the July 2024 NICE guidance update and explores hypotheses for the observed variation across ICBs.

#### Abstract

Since the 1990s, alteplase has served as the established standard of care for thrombolytic therapy in acute ischaemic stroke. It is an extremely well researched drug, with mountains of clinical evidence. The emergence of tenecteplase, a slightly modified variant with a similar underlying mechanism of action, presents a potential alternative that has created new opportunities in stroke care delivery. Updated NICE guidance in July 2024 recommends tenecteplase as a suitable, cheaper alternative with equivalent outcomes and safety. This has kicked off a period of transition in the way thrombolysis is delivered across different healthcare systems in the UK. 

Exploring regional changes represents a natural experiment in guideline implementation across different organisational contexts in the NHS. Switching to tenecteplase seems like an obvious choice: a cheaper drug, NICE approved, good clinical outcomes and easier to use. As we explain in this report, the real story is not as clear. We have noticed late adopters, ICBs with no significant adoption as well as ICBs with majority adoption, where tenecteplase use has overtaken alteplase use. ICBs vary in many ways: organisational structures, implementation capabilities, spending... the list goes on. This report aims to unpack differential adoption rates to assess how new clinical evidence trickles down from large governing boards to day to day management.   

#### Introduction

Tenecteplase offers potential advantages including single-bolus administration (reducing nursing time), improved storage stability and potentially better clinical outcomes in certain patient populations. In the UK, it's efficacy was assessed in the ATTEST-2 trial, which had the following results......

The prospect of single-bolus administration also confers some unique advantages. Thrombolysis can be started at presentation to local District General Hospitals (DGHs) before transfer to Hyperacute Stroke Units (HASUs) for thrombectomy or further care, without the need of setting up infusions which would need to be maintained during transport. As several ICBs shift to the HASU model of stroke care where all patients are transferred to specialist centres, tenecteplase provides a unique avenue in the "drip and ship" route of stroke management. 

The current differences in prices are as follows: 

Alteplase:
- 10mg powder and solvent for solution for injection vials: £172.80
- 20mg powder and solvent for solution for injection vials: £259.20
- 50mg powder and solvent for solution for infusion vials: £432.00

Tenecteplase:
- 5,000 unit (25mg) powder for solution for injection vials: £602.70
- 10,000 unit (50mg) powder and solvent for solution for injection vials: £602.70

Source for this is latest BNF data.

[View alteplase heatmap](Blog/alteplase_icb_heatmap.html)
[View tenecteplase heatmap](Blog/tenecteplase_icb_heatmap.html)

#### Methodology

Data was obtained from the Secondary Care Medicines Dataset (SCMD), which provides monthly prescribing information for NHS trusts in England. For this analysis, prescription volumes of alteplase and tenecteplase were extracted over a 24-month study period from July 2023 to June 2025, encompassing 12 months before and after the NICE guidance change.

The SCMD data structure includes:

- YEAR_MONTH: Temporal identifier
- ODS_CODE: Organisation Data Service code for each trust
- VMP_PRODUCT_NAME: Virtual Medicinal Product name
- TOTAL_QUANTITY_IN_VMP_UNIT: Volume prescribed
- INDICATIVE_COST: costs for storage of that month's inventory, calculated in the following way...

For comparison between the two drugs, we calculated defined daily doses (DDDs), which is a standardised measurement by the WHO for how much of a drug would reasonably be prescribed to a patient in one day. The DDD value for alteplase is 100mg and 40mg for tenecteplase. 

To compare prices, we used the secondary care medicines INDICATIVE_COST column divided by the number of DDDs to create a proxy cost per defined daily dose number. 

An interrupted time series (ITS) design was employed to assess the impact of the July 2024 NICE guidance change on prescribing patterns. ITS is well-suited for evaluating longitudinal effects of population-level interventions where randomisation is not feasible. The model specification was:

Y_t = β₀ + β₁_time_t + β₂_intervention_t + β₃*.time_after_intervention_t + ε_t

Where:

- Y_t = outcome at time t (DDD of thrombolytic)
- time_t = time since study start
- intervention_t = binary indicator (0 before July 2024, 1 after)
- time_after_intervention_t = time since intervention
- β₂ = immediate level change
- β₃ = change in slope post-intervention

Autocorrelation is common in ITS data due to the temporal structure of repeated measures. To ensure valid inference, we applied Newey-West heteroskedasticity and autocorrelation-consistent (HAC) standard errors. This approach adjusts the variance-covariance matrix of the estimated coefficients, providing robust standard errors under both autocorrelation and heteroskedasticity.

#### Results

- Alteplase cost per DDD: £1,177.38
- Tenecteplase cost per DDD: £781.91

This represents a potential cost saving of £395.47 per treatment episode when switching from alteplase to tenecteplase. Over the study period, total NHS expenditure was:

- Total spend on alteplase: £28,936,408
- Total spend on tenecteplase: £4,600,409

If all doses had been switched to tenecteplase during the study period, the NHS could have saved approximately £8,244,057 - sufficient funding to treat an additional 10,542 stroke patients with thrombolysis.

#### Discussion

https://www.youtube.com/watch?v=F8Fjnh3VXC0





#### Appendix

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


# References