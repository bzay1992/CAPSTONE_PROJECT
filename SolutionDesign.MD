
1.	Solution:

2.	Use Cases:
●	Which disease has a maximum number of claims.
●	Find those Subscribers having age less than 30 and they subscribe any subgroup
●	Find out which group has maximum subgroups.
●	Find out hospital which serve most number of patients
●	Find out which subgroups subscribe most number of times
●	Find out total number of claims which were rejected
●	From where most claims are coming (city)
●	Which groups of policies subscriber subscribe mostly Government or private
●	Average monthly premium subscriber pay to insurance company.
●	Find out Which group is most profitable
●	List all the patients below age of 18 who admit for cancer
●	List patients who have cashless insurance and have total charges greater than or equal for Rs. 50,000.
●	List female patients over the age of 40 that have undergone knee surgery in the past year


3.	Database Design - List down all possible db(Redshift) tables here
a.	 Tables Metadata Info with Pk/FK relationship - 
b.	 ER diagram - Optional
4.	Technologies and Platforms to be used in this solution -List down list of technologies like spark, aws and databricks etc.


2.	Database Design - 

Claims.Json

3.	Field	Data Type	Description
claim_id	Numeric (Integer)	Identifier for a specific claim.
patient_id	Numeric (Integer)	Identifier for the patient associated with the claim.
disease_name	Text	Name of the disease associated with the claim.
SUB_ID	Text	Sub-identifier for the claim.
Claim_Or_Rejected	Text	Indicates if the claim was accepted or rejected.
claim_type	Text	Type of the claim (e.g., claims of value, claims of policy, etc.).
claim_amount	Numeric (Integer)	Amount associated with the claim.
claim_date	Date	Date when the claim was made.

Group

Field	Data Type	Description
Country	Text	Country where the insurance group operates.
premium_written	Numeric (Integer)	Premium amount written by the insurance group.
zipcode	Numeric (Integer)	Zip code associated with the insurance group.
Grp_Id	Text	Identifier for the insurance group.
Grp_Name	Text	Name of the insurance group.
Grp_Type	Text	Type of the insurance group (e.g., Govt. or Private).
city	Text	City where the insurance group is located.
year	Numeric (Integer)	Year when the insurance group was established.

 
Disease
Field	Data Type	Description
SubGrpID	Text	Subgroup identifier.
Disease_ID	Numeric (Integer)	Identifier for the disease.
Disease_name	Text	Name of the disease.
		

Grpsubgrp
Field	Data Type	Description
SubGrp_ID	Text	Subgroup identifier.
Grp_Id	Text	Group identifier.


Hospital
Field	Data Type	Description
Hospital_id	Text	Identifier for the hospital.
Hospital_name	Text	Name of the hospital.
city	Text	City where the hospital is located.
state	Text	State where the hospital is located.
country	Text	Country where the hospital is located.


Patient_records
Field	Data Type	Description
Patient_id	Numeric (Integer)	Identifier for the patient.
Patient_name	Text	Name of the patient.
patient_gender	Text	Gender of the patient.
patient_birth_date	Date	Birth date of the patient.
patient_phone	Text	Phone number of the patient.
disease_name	Text	Name of the disease.
city	Text	City where the patient is located.
hospital_id	Text	Identifier for the hospital.

Subgroup
Field	Data Type	Description
SubGrp_id	Text	Identifier for the subgroup.
SubGrp_Name	Text	Name of the subgroup.
Monthly_Premium	Numeric (Integer)	Monthly premium associated with the subgroup.

Subscriber
Field	Data Type	Description
sub_id	Text	Identifier for the subscriber.
first_name	Text	First name of the subscriber.
last_name	Text	Last name of the subscriber.
Street	Text	Street address of the subscriber.
Birth_date	Date	Date of birth of the subscriber.
Gender	Text	Gender of the subscriber.
Phone	Text	Phone number of the subscriber.
Country	Text	Country of residence of the subscriber.
City	Text	City of residence of the subscriber.
Zip Code	Text	Zip Code of the subscriber.
Subgrp_id	Text	Identifier for the subscription group.
Elig_ind	Text	Eligibility indicator (Y/N) for subscription.
eff_date	Date	Effective date of subscription.
term_date	Date	Termination date of subscription.

