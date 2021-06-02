# UDACITY | Data Analyst Nanodegree Program
# Communicate Data Findings: Express Entry Permanent Residence Applications Data Exploration

## Overview

This project has two parts that demonstrate the importance and value of data visualization techniques in the data analysis process. In the first part, I used Python visualization libraries to explore a selected dataset, starting from plots of single variables and building up to plots of multiple variables. In the second part, I produced a short presentation that illustrates interesting properties, trends, and relationships that I discovered in the dataset. The primary method of conveying my findings was through transforming your exploratory visualizations from the first part into polished, explanatory visualizations.

I gathered data, then assessed and cleaned the data and stored it in [*cases_master.csv*](https://github.com/aquamila/UDACITY_DAND_Communicate_Data_Findings/blob/main/cases_master.csv). Then I [explored the dataset](https://github.com/aquamila/UDACITY_DAND_Communicate_Data_Findings/blob/main/exploratory_data_analysis.ipynb) and [communicated my findings it](https://github.com/aquamila/UDACITY_DAND_Communicate_Data_Findings/blob/main/communicate_data_findings.ipynb).

, analyzed the dataset and then communicated my findings about it in act_report.pdf. 

I gathered data and stored it in [*cases_master.csv*](https://github.com/aquamila/UDACITY_DAND_Communicate_Data_Findings/blob/main/cases_master.csv), then assessed and cleaned data, analyzed the dataset and then communicated my findings about it in act_report.pdf.

I shared all the steps in the Jupiter Notebook file wrangle_act.ipynb and in wrangle_report.pdf in a summary form

## Dataset

The subject of this exploration analysis is an Canadian Immigration Express Entry Permanent Residence Applications dataset from [MyImmigrationTracker](https://www.myimmitracker.com). 

MyImmiTrackeris a collaborative community project which allows immigrant applicants to enter and then track and analyze the progress of their applications.

Express Entry is a system used by the Canadian government to manage applications for Canadian permanent residence through certain economic immigration programs: Federal Skilled Workers (FSW), Canadian Experience Class (CEC) and Provincial Nominee Program (PNP).

The dataset containing more than 19,000 immigration complete and incomplete cases covering the period from April, 2015 to August, 2019. All dates and statuses of the incomplete cases are valid at the time of gathering data on August 6, 2019.

The raw dataset was cleaned and stored in [*cases_master.csv*](https://github.com/aquamila/UDACITY_DAND_Communicate_Data_Findings/blob/main/cases_master.csv) for further analysis.

There are 19,193 cases in the dataset with 16 features. 

One part of them describes the applicantion case:   

**case** - the unique applicantion case id   
**stream** - the name of the applicant's immigration program: FSW-Outland, FSW-Inland, CEC, PNP-Outland, PNP-Inland    
**current_status** - the current status of the application case in terms of mandatory processing stages: e-APR AOR, Medicals Passed, PPR/Refused      
**dependents** - the number of applicant's family members who immigrate as well       
**province**  - the name of the province for the applicantions with provincial nominations (PNP-Outland and PNP-Inland streams)      
**nationality** - the applicant's country of nationality      
**residence** - the applicant's country of residence      
**visa_office** - the office where applicantion case is/were processing      
**final_decision** - whether the case was approved (PPR) or refused (Refused)

The other part reflects dates of application processing stages completion:             

**aor_date** - the date when application documents were submitted (mandatory)   
**med_passed_date**  - the date when applicant's medical examination were approved (mandatory)                  
**add_docs_request_date** - the date when additional documents were requested if there was this stage (optional)     
**rprf_paid_date** - the date when applicant paid processing fee (mandatory)          
**ss_start_date** - the date when security screening was started if there was this stage (optional)        
**final_decision_date** - the date when the case was approved or refused (mandatory)     

The last features describes applicant's profile activity on [MyImmigrationTracker](https://www.myimmitracker.com):   

**state** - whether there has been any activity on the applicant's profile in the last 2 months     

Most variables are categorical nominal and ordinal and all dates are date/time variables.


## Summary of Findings

The main goal of the analysis was to find out the application case features which affect on application processing time.

I investigated the next case features: 

- the name of the applicant's immigration program (stream)
- the number of applicant's family members (dependents)
- the applicant's countries of nationality and residence (nationality and residence)
- the office where applicantion case were processing (visa_office) 
- whether the case was approved (PPR) or refused (Refused) (final_decision)
- whether the case had optional processing stages like additional documents request and security screening 
- processing time in days 

As I found out not all applications case features have noticeable effect on processing time. The most crucial factors as the investigation showed are:

- the presence of optional processing stages: additional documents request and security screening (the combination of them maximizes processing time);
- the citizenship or residence in Iran, Iraq, Lebanon, Palestine, Syrian Arabic Republic, Jordan, Libya;
- immigration to Canada through Provincial Nominee Program especially if the future immigrant applies from inside Canada.
