 # **Software Requirements Specification**  
**for Volunteer Management System**  
**Version 1.3**  

** approved **  

*Prepared by Cooper, Heather, and Trevor*  
*TRU students*  
*2022-11-28*  

| **Table of Contents** |
| ----------- |
| 1. Introduction	 |
| 1.1 Purpose	 |
| 1.2 Document Conventions	 |
| 1.3 Intended Audience and Reading Suggestions	 |
| 1.4 Product Scope	 |
| 1.5 References	 |
| 2. Overall Description	 |
| 2.1 Product Perspective	 |
| 2.2 Product Functions	 |
| 2.3 User Classes and Characteristics	 |
| 2.4 Operating Environment	 |
| 2.5 Design and Implementation Constraints	 |
| 2.6 User Documentation	 |
| 2.7 Assumptions and Dependencies	 |
| 3. External Interface Requirements	 |
| 3.1 User Interfaces	 |
| 3.2 Hardware Interfaces	 |
| 3.3 Software Interfaces	 |
| 3.4 Communications Interfaces	 |
| 4. System Features	 |
| 4.1 Assign Volunteer	 |
| 4.2 Create New Volunteer	 |
| 4.3 Generate Daily Report	 |
| 5. Other Nonfunctional Requirements	 |
| 5.1 Non Functional Requirements	 |
| 5.2 Performance Requirements	 |
| 5.3 Safety Requirements	 |
| 5.4 Security Requirements	 |
| 5.5 Software Quality Attributes	 |
| 5.6 Business Rules	 |
| 6. Other Requirements |

**Revision History**

| **Name** | **Date** | **Reason For Changes** | **Version** |
| :- | :- | :- | :- |
| Cooper | 2022-11-0 | New information | 1.0 |
| Heather | 2022-11-04 | New information | 1.1 |
| Trevor | 2022-11-06  New information | 1.2 |
| Cooper | 2022-11-20| New information on non-functional requirements | 1.3 |


# Introduction
## Purpose 
The product specified in this document is a volunteer management system. The current approved  revision for this product is 1.2. The scope for this product that is covered by this SRS is the entire piece of software.


## Document Conventions
We have bolded important words or sentences that are of higher priority or importance. 

## Intended Audience and Reading Suggestions
This document is written for developers, testers, and documentation writers. The reset of the SRS contains: overall description, external interface requirements, and system features. We suggest you read from start to finish no matter the reader type.
## Product Scope
Refer to vision and scope document

## References
AB. Burak. “Your 2022 Guide to Writing a Software Requirements Specification (SRS) Document” Relevant. https://relevant.software/blog/software-requirements-specification-srs-document/(2022-11-25)




# Overall Description
## Product Perspective
This product is an original product with no affiliation to a lineup of other products. Nor is it a component of a larger product.
## Product Functions
**Functional Requirements for UC1: Create New Volunteer**
Using hierarchical textual tags


* ID: Create.Details
Description: The system shall allow users to enter the personal details: full name, phone number, email, address, availability, and volunteer interests.

* ID: Create.Save
Description:The system shall allow users to save their progress in the application process. 

* ID: Create.Recover
Description:The shall allow users to retrieve their progress in the application process. 

* ID: Create.PoliceSend
Description:The system shall send the volunteer data to the police system.

* ID: Create.PoliceReject
Description:The system shall contact the volunteer if their status is rejected by police system

* ID: Create.PoliceAccept
Description:The system shall contact the volunteer if their status is accepted by police system

* ID: Create.AdminSend
Description:The system shall send the volunteer data to the administrator if the volunteer wants to work with students.

* ID: Create.AdminReject
Description: The system shall contact the volunteer if their status is rejected by administration

* ID: Create.Appeal
Description:If rejected the system shall give the volunteer contact information of the administrator to appeal.


**Functional Requirements for UC3: Generate Daily Report**


* ID: view.TodayNumberofDailyRequests
Description: The system shall show how many seniors needed assistance on this day

* ID: view.TodayNumberofDailyRequestsFilled
Description: The system shall show how many seniors received the help they needed this day

* ID: view.TodayNumberofVolunteersScheduled
Description: The system shall show how many volunteers were scheduled to work this day

* ID: view.TodayNumberofVolunteersWorked
Description: The system shall show how many volunteers did work this day

* ID: view.TodayNumberofVolunteersNoShow
Description: The system shall show how many volunteers did not work today who were scheduled

* ID: view.TodayNumberofCasesUnfilled
Description: The system shall show how many seniors needing assistance did not get help today

* ID: view.TodayNumberofVolunteersAdded
Description: The system shall show how many new volunteers were added today

* ID: view.TodayNumberofRequestsAdded
Description: The system shall show how many new requests from seniors for assistance were added today

* ID: view.NextDayNumberofRequests
Description: The system shall show how many seniors are needing assistance tomorrow

* ID: view.NextDayNumberofVolunteersScheduled
Description: The system shall show how many volunteers are scheduled to work tomorrow

* ID: view.NextDayShortageAnticipated
Description: The system shall show how many volunteers will the VMS be short tomorrow 


**Functional Requirements for UC4: Assign Volunteer**

Using hierarchical textual tags


* ID: Fetch.Seniorlist
Description: The system shall display a list of seniors in need of support starting with the highest priority

* ID: Fetch.Volunteerlist
Description: The system shall display a list of suitable volunteers for prospective seniors.

* ID: Fetch.SeniorInformation
Description: The system shall display name, age, problems, interest, location, and phone number or selected senior. 

* ID: View.Volunteeringhistory
Description: The system shall show volunteer history to SPCC employees to help decide on pairings.

* ID: Send.VolunteerInformation
Description: The system shall send volunteer information to SPCC employees so they can better pair seniors to volunteers.

* ID: Send.Volunteerrequest
Description: The system shall notify the volunteer that their service has been requested.

* ID: Get.Volunteerresponse
Description: The System shall receives the response from the volunteer which could include the request for a different schedule or them rejecting the request

* ID: Fetch.Volunteerresponse
Description: The system shall show the SPCC employee the volunteer response.


# User Classes and Characteristics

| User | User class | Description |
| :- | :- | :- |
| Volunteers | Direct, favored | These persons will have passed their background check and be available for volunteer services. They will enter their available hours into the VMS for the administrators to view and assign to a senior. Once they have completed the assigned task, they will enter into the VMS a short description of the duties performed and the outcome. |
| Administrators | Direct, favored | Administrators will use the system to review available volunteers and seniors needing assistance. They will be able to assign available volunteers to upcoming cases and review the outcomes of completed volunteer duties. The VMS will also notify them when there are more requests for assistance than volunteers available. They will have access to details on all seniors and all volunteers, unlike other volunteers and seniors who will only have access to their own data. |
| Seniors | Direct, favored | Once registered with the city, seniors will be able to submit requests for assistance directly to the VMS or have their request entered through an administrator. The seniors will only have access to their own data and will have a simple portal to facilitate the request for a volunteer. They will be notified when a volunteer is assigned and given the name of the person to expect. |
| Mayoral Office | Direct, favored | The mayoral office will be able to access all the features of the administrators and see some data logging as well, indicating the numbers of requests, numbers of filled requests, and some trending to indicate typical times when requests for service are higher or volunteers are in short supply. This will help the mayoral office to coordinate the search for volunteers and verify that the system is working effectively. |
| Business Owners | Indirect, favored| Business owners will not interact with the system directly but will benefit from its success in the form of increased activity in the downtown area, hopefully leading to a reduction in crime and increase in sales revenue.  |
| Background Check Administrators | Indirect, ignored | Background check administrators will need to submit background check pass/fail results to the VMS. They will only need access to the data of the volunteer applicants that is necessary to perform the background checks. Their satisfaction is not important to the success of the project, as long as they can submit their data in a timely manner. |
| Individuals who cannot pass the background check | Disfavoured, direct | These individuals are not desired as part of the volunteer pool, and should only have access to the system to apply for volunteer status. Following the rejection of the background check, they should not have any access to the system unless a malfunction of an error on the part of the background check system has occurred. |
|Individuals wanting help around the house who are not seniors | Disfavoured, direct | These individuals are not currently a part of the group being serviced by the VMS. Currently the system is only providing help to seniors, not anyone who wants help around the house. When registering with the city, seniors will need to provide their date of birth with a piece of ID for confirmation. Anyone who cannot provide these documents should not be able to gain access to the system. |
| Students | Disfavoured, indirect | In future, the VMS may be expanded to help provide students with additional tutoring services. In this case, the students requiring help would be matched with qualified tutors. These students would likely not use the VMS directly but schools would be able to draw on a tutor bank to request help for special cases where additional tutoring is required in addition to the online resources students already have available. |


## Operating Environment
This software will operate on Windows 10-11, macOS Sierra, and Ubuntu 22.10. It will work on any computer with these systems from 2017 and onward. 

## Design and Implementation Constraints
The software must be able to run on a computer with only 4 gigabytes of ram and a CPU with minimum 1.5GHz. 

## User Documentation
No user documentation or tutorials as of this version

## Assumptions and Dependencies
We are assuming the people using this product will have basic computer skills and knowledge or access to an IT team to help. We assume that it will be used by only adults and not children. 

# External Interface Requirements

## User Interfaces
User interface prototype layout design:

Main Page

![alt text](https://user-images.githubusercontent.com/119646667/205228523-1e52acad-6183-4c03-a404-40d59b072af7.png " Main Page ")


Volunteer list

![alt text](https://user-images.githubusercontent.com/119646667/205228443-b4f8b896-2279-4595-baae-3eb694be2fd7.png " Volunteer List ")



Volunteer page

![alt text](https://user-images.githubusercontent.com/119646667/205228071-d768568c-7959-4cd9-9086-8929b42ab704.png " Volunteer Page ")


## Hardware Interfaces
HI 1.1 -The VMS will be built to run on desktop computers only. It will be built for Windows and Mac OS. There will be no smartphone or other hardware platform options. Restricting the system access to desktop computers will help keep data safe. It will also keep development costs down and make future modifications more simple.

## Software Interfaces
SI 1.1 - VMS will interface with current Windows and MAC OS as it will be a desktop application running on these platforms.


SI 1.2 - The system will need to interface programmatically with the system that processes criminal record checks, to verify when volunteers have been approved and can be added to the database as active and available. 


SI 1.3 - The system will also have to interface with an external database for storing data on 
volunteers and assistance requests. This will be done using SQLServer and will allow multiple administrators to access the system and historical data as needed without wasting disk space.

## Communications Interfaces
CI 1.1 - VMS will interface with google email platform (Gmail) to send administrator daily reports.
CI 1.2 - VMS will interface with google email platform to send volunteers emails when they have been assigned to a case

# System Features

## Assign Volunteer
###	Description and Priority
This feature takes volunteers who have passed the background check and assigns them to either
a senior in need or a school in need of a tutor. Each volunteer is assigned to a case manually by a system administrator, from a list of available and capable volunteers generated by the VMS. The administrator has access to the volunteer history of each volunteer, which will assist in making a decision.

Priority Component Rating
Benefit: 9
Cost: 6
Risk: 2
Penalty: 2

### Stimulus/Response Sequences
An administrator will log a seniors request for volunteer support.
The system will generate a list of available volunteers to display for the administrator, and the pertinent information on each (volunteer history, volunteer engagement score)
After reviewing available volunteers, the administrator will then select a fitting and available volunteer from the list.
The chosen volunteer will receive an email notifying them that they have been assigned to a case, containing all pertinent details on the job (location, time, nature of work, names of seniors to be assisted, etc)

3.1.3	Functional Requirements

ID: Fetch.Seniorlist

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| The system has to have 1 or more available requests in senior list | If the system has no patients in senior list display error message
“There are no available patients in senior list Error #1893”
System must fetch the senior list within a reasonable time such as under 20 seconds
System did not fetch list within 20 seconds display error message
“Fetching senior list timed out
Error #8931” |



ID: Fetch.Volunteerlist

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| The system has to have 1 or more available volunteers in volunteer list | If the system has no volunteers in volunteer list display error message
“There are no available volunteers in volunteer list Error #1894”
System must fetch the volunteer list within a reasonable time such as under 20 seconds
System did not fetch list within 20 seconds display error message
“Fetching volunteer list timed out
Error #8932” |

REQ-1:
ID: Fetch.SeniorInformation

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| Seniors information must contain valid characters
If there are invalid characters in senior information display error message
“Senior information contains invalid characters Error #1742”
System must be fetching a senior within the system | If the system cannot find the senior the user requested then display error message
“The senior information you requested could not be found Error #2109”
System must fetch the senior information within a reasonable time such as under 20 seconds
System did not fetch information within 20 seconds display error message
“Fetching senior information timed out
Error #8932” |


REQ-2:
ID: View.Volunteeringhistory


| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| Volunteers history must contain valid characters
If there are invalid characters in senior information display error message
“Senior information contains invalid characters Error #1242”
System must be fetching a volunteer within the system | If the system cannot find the volunteer the user requested then display error message
“The volunteer history you requested could not be found Error #2849”
System must fetch the volunteers history within a reasonable time such as under 20 seconds
System did not fetch history within 20 seconds display error message
“Fetching volunteer history timed out
Error #8512” |


REQ-3:
ID: Send.VolunteerInformation

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must check if it is sending a valid volunteer
If the volunteer the system is trying to send is invalid such as volunteer is not in system | “Volunteer information could not be sent. Invalid volunteer Error #1275”
System must send the volunteers information within a reasonable time such as under 20 seconds
System did not send information within 20 seconds display error message
“Sending volunteer informational timed out
Error #8512” |


REQ-4:
ID: Send.Volunteerrequest


| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System will send automated request to volunteer
If the request fails to send | “Volunteer requests could not be sent 
Error #1475” System must send the request within a reasonable time such as under 20 seconds
System did not send information within 20 seconds display error message
“Sending requestl timed out
Error #7512” |


REQ-5:
ID: Fetch.Volunteerresponse

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System receive response and stores response in list| If the system fails to receive response by the list becoming full
“System failed to receive a response. List is overloaded
Error #1255” |


## Create New Volunteer
### Description and Priority
System receives volunteers information and creates new volunteer which will be added to the system
Priority Component Rating
 * Benefit: 7
 * Cost: 4
 * Risk: 3
 * Penalty: 3


###	Stimulus/Response Sequences
1. Firstly a volunteer will create an account though the VMS
2. This account is then shared between the VMS and the SPCC employee
3. This account will then be recorded within the volunteer list

###	Functional Requirements

ID: Create.Details
Description: The system shall allow users to enter the personal details: full name, phone number, email, address, availability, and volunteer interests.

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must check for invalid characters that the volunteer tries to input | If any sections contains invalid characters then display error message “System detected invalid character Error #1832” |
| System must check if there are any missing sections |If a section is left blank then display error message “System detected missing section Error #8272” |


ID: Create.Save
Description:The system shall allow users to save their progress in the application process. 

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System saves the users progress and stores it in a database | If the save happens to get corrupted or does not save properly “System failed to save progress Error #8231” |


ID: Create.Recover
Description:The shall allow users to retrieve their progress in the application process. 

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves the save and fills in the information | If the system fails to fetch the information display error message “System failed to fetch progress Error #1622” |


ID: Create.PoliceSend
Description:The system shall send the volunteer data to the police system.

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must receive and send the volunteers information with 1 minute from when the volunteer account was created |If the system is too slow to send the information then it will be sent manually by a operator “System is overloaded and failed to send information” Error #1342” |


ID: Create.PoliceReject
Description:The system shall contact the volunteer if their status is rejected by police system

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must be able to store 1000 police response and send a automated response to volunteer |If the system is full and another response is sent to the system display error message “System is overloaded and failed to accept response” Error #1642” |


ID: Create.PoliceAccept
Description:The system shall contact the volunteer if their status is accepted by police system

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must be able to store 1000 police response and send a automated response to volunteer | If the system is full and another response is sent to the system display error message “System is overloaded and failed to accept response” Error #1242” |


ID: Create.AdminSend
Description:The system shall send the volunteer data to the administrator if the volunteer wants to work with students.

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System looks for matching volunteer and sends their data to the administrator | If the system cannot find the volunteer of fails to send data “System failed to send volunteer data to admin” Error #1342” |


ID: Create.AdminReject
Description: The system shall contact the volunteer if their status is rejected by administration

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must be able to store 1000 admin response  | If the system is full of admin responses display error message “System is overloaded” Error #1142” |


## Generate Daily Report
###	Description and Priority
Triggered by the end of day (23:59) the VMS system will send a report to system administrators with all valid statistics gathered for the day’s operations, and some projections for tomorrow.
Priority Component Rating
 * Benefit: 7
 * Cost: 4
 * Risk: 3
 * Penalty: 3


###	Stimulus/Response Sequences
Triggered at 23:59, system will generate daily report
Report is emailed to all system administrators
If a volunteer shortage is anticipated for next day, email is marked “URGENT”

###	Functional Requirements

ID: view.TodayNumberofDailyRequests
Description: How many seniors needed assistance on this day

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System must tally all requests for assistance from seniors wanting assistance on this day | No requests for help from seniors for this particular day. Error #3321 |


ID: view.TodayNumberofDailyRequestsFilled
Description: How many seniors received the help they needed this day

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| Software tracks how many of the requests that needed assistance on this day were filled | No requests for this day or no filled requests. Error #3322 |


ID: view.TodayNumberOfVolunteersScheduled
Description: How many volunteers were scheduled to work this day

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves the number of volunteers who where assigned to work this day | No volunteers available or assigned to any cases this day. Error #3323 |


ID: view.TodayNumberofVolunteersWorked
Description: How many volunteers did work this day

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves how many volunteers actually filled the service requests they were assigned to this day | No volunteers did work this day. Error #3324 |


ID: view.TodayNumberofVolunteersNoShow
Description: How many volunteers did not work today who were scheduled

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves how many volunteers did not complete the tasks they were assigned to this day | None |


ID: view.TodayNumberofCasesUnfilled
Description: How many seniors needing assistance did not get help today

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves how many cases went unfilled this day | None |


ID: view.TodayNumberofVolunteersAdded
Description: How many new volunteers were added today

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves number of new volunteers added to system today | None |


ID: view.TodayNumberofRequestsAdded
Description: How many new requests from seniors for assistance were added today

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves number of new requests added to system today | No new requests were made this day. Error #3325 |




ID: view.NextDayNumberofRequests
Description: How many seniors are needing assistance tomorrow

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves number of requests for assistance needing to be filled tomorrow | No requests for help need to be filled tomorrow. Error #3326 |


ID: view.NextDayNumberOfVolunteersScheduled
Description: How many volunteers are scheduled to work tomorrow

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System retrieves number of volunteers scheduled to work tomorrow | No volunteers scheduled to work tomorrow. Error #3327 |


ID: view.NextDayShortageAnticipated
Description: How many volunteers will the VMS be short tomorrow (if any)

| Software Capabilities | Error Conditions or Invalid Inputs |
| :- | :- |
| System finds difference between number of cases needing assistance tomorrow and number of volunteers scheduled to work. Reports difference, if there are too few volunteers available to complete the needed requests. | None |


## 	QFD Prioritization Of Requirements

| Relative Weights | 2 | 1 | - | - |0.5 | - | - |1 | - | - |
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Feature| Relative benefit | Relative penalty | Total value | Total value | Value % | Relative cost | Cost % | Relative risk | Risk % | Priority |
| 6 | Modify volunteer data | 3 | 5 | 11 | 10.6 | 1 | 2.9 | 1 | 3.6 | 2.717948718 |
| 3 | Assign volunteer | 9 | 9 | 27 | 26 | 7 | 20.6 | 1 | 3.6 | 1.203703704 |
| 5 | Record a volunteer progress report | 7 | 3 | 17 | 16.3 | 5 | 14.7 | 3 | 10.7 | 0.9209039548 |
| 1 | Create senior-peer volunteer | 9 | 9 | 27 | 26 | 7 | 20.6 | 9 | 32.1 | 0.8783783784 |
| 4 | Generate daily reports | 5 | 9 | 19 | 18.3 | 7 | 20.6 | 5 | 17.9 | 0.71484375 |
| 2 | Create student-peer volunteer | 1 | 1 | 4 | 3.8 | 7 | 20.6 | 9 | 32.1 | 0.1283783784 |
| **Totals** | **34** | **36** | **104** |  | **34** | :- | **28** | :- | :- | :- |




# Other Nonfunctional Requirements

## Non Functional Requirements

|Non-Functional Requirement| Quality Attribute |
| :- | :- |
| The system shall be very fast | Performance |
| The system shall be easy to learn | Usability |
| The system shall be easy to use | Usability |
| The system shall keep senior people’s data hidden from volunteers | Security |


## Performance Requirements
 * Track 60% of the senior cases in the city
 * Provide support to 85% of the reported cases
 * Manage around 10-15k cases at a time
 * Reduce volunteer assignment time to three days
 * Track individual volunteer engagement as a numerical figure

## Safety Requirements
 * Must ensure that no volunteer can be assigned to a vulnerable person (senior, student) without passing a criminal record check
 * Must ensure that no volunteer can access data on any other user prior to passing a criminal record check
 * Must ensure that volunteers are not assigned to duties they are medically unable to perform (eg. heavy lifting)

## Security Requirements
* Must securely maintain personal data on users (volunteers, seniors, students). Encryption for data and strong password protection for administrators will be essential
* Will not collect or store any personal information that is not required for the VMS service
* Software Quality Attributes

### External Quality Attributes

1. VMS will be easy to install on customer computer, with an installation wizard to walk them through the process
2. VMS will be easy to update on customer computer using a simple button
3. VMS will be user-friendly, and with a help function and user manual, administrators should be able to learn the system in under one day
4. System will perform well to unexpected situations with detailed error or warning messages in the event of a failure

### Internal Quality Attributes

1. System will be built to easily allow for expansion of features (such as tutoring) saving at least 40% of cost on future additions
2. VMS will be built for Windows and Apple OS.
3. Modular software will be reusable, for the VMS and future projects as well.

A = Availability
I = Integrity
P = Performance
R = Reliability
Ro = Robustness
S = Security
U = Usability
I = Interoperability

| Attribute | Score | A | I | P | R |Ro | S | U | It | 
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | 
| A | 4 | :- | < | ^ | ^ | ^ | ^ | < | ^ | 
| I | 3 | :- | :- | ^ | ^ | ^ | ^ | ^ | ^ |
| P | 7 | :- | :- | :- | < | < | ^ | < | < |
| R | 6 | :- | :- | :- | :- | < | ^ | < | ^ |
| Ro | 5 | :- | :- | :- | :- | :- | ^ | < | ^ |
| S | 7 | :- | :- | :- | :- | :- | :- | < | ^ |
| U | 3 | :- | :- | :- | :- | :- | :- | :- | < |
| It | 7 | :- | :- | :- | :- | :- | :- | :- | :- |



**Availability**
The VMS should be available for 90% of working hours (6am to 4pm) and be available for another 2 hours in the case where people come in for overtime or want to stay late.

**Integrity**
The system should ensure it has the right information before it assigns a volunteer and before  sending information to the background checking system.

**Performance**
The VMS should fetch information within 2 seconds and send information to the background checking system within 5 seconds.

**Reliability**
The system should not encounter more than 2 errors per year.

**Robustness**
When entering an invalid input the system should continue to function properly and display a message of a valid input.

**Security**
Outside sources should not be able to get ahold of volunteer and patient information. The system should also have protection for viruses and security attacks.

**Usability**
New workers should only have to spend 1 week learning the system, in other words it should be easy to learn and work on.

**Interoperability**
The system should easily be able to exchange data with the background checking system. It should also be easy to access the data the system receives.

## Business Rules
 * Social security numbers will be deleted after receipt of successful background check
 * Volunteers will need to pass a bi-annual background check to continue working
 * Volunteers can complete a maximum of 7 cases a week (to prevent burnout)
 * Volunteers must assist with a case at least once every 6 months, or they will be removed from the system
 * Volunteers will be removed from the system following 2 consecutive no-shows

# Other Requirements
There are no other requirements at this time

# Appendix A: Glossary
VMS: Volunteer Management System

# Appendix B: Analysis Models
Fig 1. VMS data model

![alt text](https://user-images.githubusercontent.com/119646667/205227454-07ababf1-e740-4d48-ac1a-75a1a24a5a5a.png "VMS Data Model")


**Table 1. Data Dictionary**

| Data Element | Description | Composition or Data Type | Length | Values | 
| :- | :- | :- | :- | :- | 
| Volunteer Name | Name of Volunteer | String | 40 chars | - |
| Available days | Days of week when volunteer is available | Array of bool[] | Array is of length 7 | Bool is true when volunteers are available, false when not. |
| Available times | Times available on days selected | float | 2 floats per day day available (start time, end time) | 0.00-23.59 |
| Available dates | Day of  the week when volunteer is available to work | String/YYYY-MM-DD | 10 | 2022-11-07 |
| Criminal record check result | pass/fail | Bool | 1 | 0 or 1 |
| Volunteer Information | All volunteer information | String/ Volunteer Name Available Times Criminal Record Check Result | 250 chars | In paragraph or list form |




# Appendix C: To Be Determined List
TBD
