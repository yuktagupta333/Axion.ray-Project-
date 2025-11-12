❖ Data Task 1 Report :- Data Tagging  
 
I used a straightforward, oneword classification system to tag each of the following fields:  
Root Cause, Symptom Condition, Symptom Component,  Fix Condition, and Fix Component. 
A root cause is the primary reason for the complaint, such as "Loose,
" "Faulty," or "Missing." 
The technician's diagnosis or initial failure mode provided this  information. 
Conditions and actions that may be observed, such as "Leaking," "Dri pping," or "Inactive," are examples of symptoms.This information was  derived from the particular issue that the technician or client had de scribed. 
Component of the symptom: The equipment component that is imp
acted, such as the "Sensor," "Fuel Door," or "Coupler." 
Fix condition: The repair work's service or remedial measure, such as  "Replaced," "Installed," or "Retorqued."The technicians' resolve acts served as the foundation for the corrective activity. 
Fix component: The system or part that has been fixed or replaced, s uch as the "O-Ring," "Harness," or "Bracket." 
This piece of equipment was connected to the fix condition for descri ption tracing transparency. By utilizing context 
appropriate language and sticking to a straightforward phrasing conv ention that was pertinent to the analysis classification, I was able to p reserve consistency. 
B. Possible Perspectives (potential insights) 
 Several insightful discoveries are made possible by this tagging framework: Failure Pattern Recognition: Targeted process changes are made possible by r epeated root causes such as "Loose" or "Faulty," which point to systemic prob lems in manufacturing or quality control.                         
Component RiskMapping: Parts that might need design improvements or hig her supplier quality are highlighted by frequent references to "ORing," "Senso r," and "Harness." 
Service Optimization: Field technician training programs and inventory planni ng can benefit from the use of common fix actions like "Replaced" or "Retorq ued." 
Predictive maintenance can reduce downtime and increase customer satisfac tion by using predictive models that are constructed using enough labeled da ta to predict         breakdowns based on symptom patterns. 
                                                                                                                                                                               **❖ Data Task 2 Report: Steering Wheel Repair Dataset Analysis **
A. Column Analysis 
The dataset contains over 60 columns spanning vehicle identifiers, repair details, customer complaints, dealer information, and diagnostic outcomes. Key column types include: 
 
Identifiers: VIN, TRANSACTION_ID, REPAIRING_DEALER_CODE 
Repair Details: REPAIR_DATE, GLOBAL_LABOR_CODE_DESCRIPTION, TOTALCOST, LBRCOST 
Customer Feedback: CUSTOMER_VERBATIM, CORRECTION_VERBATIM 
Vehicle Specs: ENGINE_DESC, TRANSMISSION_DESC, BODY_STYLE 
Dealer Info: DEALER_NAME, REPAIR_DLR_CITY, STATE 
 
Every column was evaluated for: 
 Data type (datetime, float, or object) 
Uniqueness (e.g., labor codes are repeated, VINs are unique) missing values (more than 50% of some columns were null). 
Relevance to business (for example, TOTALCOST and CUSTOMER_VERBATIM are essential for sentiment and cost analysis) 
 
 
 
B. Data Cleaning Summary 
Missing Values: Columns that were missing more than 50% were removed. The mode (categorical) and median (numerical) were used to impute the r emaining nulls. 
Text Standardization: In order to address discrepancies, categorical fields were capitalized and cleared of whitespace. 
Date Parsing: Month was obtained by converting REPAIR_DATE to datetim e format. 
Outlier Removal: To eliminate extreme values, IQR filtering was applied to TOTALCOST and LBRCOST. 
Free Text Processing: CORRECTION and CUSTOMER_VERBATIMTokenizing VERBATIM allowed for the extraction of tags. 
C. Visualizations  
1.	Distribution of Repair Costs:The majority of repairs cost less than ₹500,  but a small number cost more than ₹1000, according to a TOTALCOST  histogram that has a right-skewed distribution.  
2.	Most Popular Repair Types:"STEERING WHEEL REPLACEMENT" is the most common repair type, according to the bar plot of GLOBAL_LABOR_CODE_DES CRIPTION.  
3.	The Monthly Repair Volume: Time-series bar chart indicates that January– February 2024 saw the highest repair activity, which may indicate batchrelated or seasonal problems. 
D. Generated Tags & Key Takeaways  Tags Extracted 
From free-text fields, we generated tags like: 
•	Failure Tags: HEATED, INOP, BUTTON, STITCHING, PEELING 
•	Component Tags: STEERING, MODULE, TRIM, COVER 
•	Action Tags: REPLACED, CHECKED, VERIFIED, ORDERED 
•	Bonus Tags: PRA, PREAUTH, GM AUTHORIZATION, VIDEO, TRANSIT DAMAGE, REPROGRAMMED 
These tags were added to each record for quick filtering and summarization. 
 
 
* Bonus Insights & Recommendations 
 
* Unique & Meaningful Tags 1. Procedural Tags 
REPLACED, INSTALLED, TORQUED, CLEARED, RETESTED, VERIFIED, 
DIAGNOSIS, CHECKED, REMOVE, ORDERED 
These indicate technician workflows and repair validation steps, useful for process optimization. 
2.Warranty & Authorization Tags 
PRA, PREAUTH, GM AUTHORIZATION, SOP, RO, CLAIM APPROVED 
These reflect warranty approval processes and service order tracking, critical for compliance and cost recovery. 
3.Customer Behavior Tags 
VIDEO, ADVISOR, INSPECT, REPORT, CONFIRMED, REQUESTED 
 
* Insights 
1.The most common problem is heated steering wheel failures. 
2.All versions have common material flaws like peeling and stitching. 
3.More than 60% of records have warranty tags (PRA, PREAUTH). 
 
* Recommendations 
1.Enhance Component Quality: Pay attention to stitching durability and hot  modules. 
2.Automate Warranty Workflows: To expedite approvals, use PRA tags. 
3.Standardize Dealer Repairs: Use procedural tags to reinforce SOPs. 
 
 
