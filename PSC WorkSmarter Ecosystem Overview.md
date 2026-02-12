# PSC WorkSmarter Ecosystem Overview



## Table of Contents

- [Introduction](#introduction)
- [Integrations](#integrations)
  - [PRICES](#PRICES)
  - [HCAS PRISM](#HCAS-PRISM)
  - [FBIS](#FBIS)
  - [DocuSign](#DocuSign)
  - [AMS](#AMS)
- [Platform-wide Utilities](#Platform-wide-Utilities)
  - [Help Desk](#Help-Desk)
  - [Knowledge Gateway](#Knowledge-Gateway)
- [Applications](#Applications)
  - [Acquisition Reporting System (ARS)](#acquisition-reporting-system-ars)
  - [Customer Agreement Module (CAM)](customer-agreement-module-cam)
  - [ResourceFlow Formulation/Execution](#resourceflow-formulation/execution)
  - [Unified Dynamic Case Management (UDCM)](#unified-dynamic-case-management-udcm)
  - [Position Description Management (PDM)](#position-description-management-pdm)
  - [Workflow Automation](#workflow-automation)
- [Questions](#questions)



## Introduction

PSC WorkSmarter is an application hosting platform that is owned by the PSC Office of the Director. The platform is composed of the Appian business process modelling platform, the Blue Prism robotic process automation (RPA) suite, and Oracle database. The platform hosts systems which are owned by various HHS StaffDivs. It has an authorization to operate (ATO) from the HHS Chief Information Security Officer, meaning that the process to release new systems on the platform to production is considerably streamlined compared to the task of implementing a new, standalone system.

The platform also has the following shared, platform-wide features that are available to the individual users of the various systems:

- Help Desk support/ticketing module for use by production support teams for the applications
- Several applications made specifically for WorkSmarter
- Knowledge Gateway document repository
- Multi-Factor Authentication capabilities via integration with the HHS Management System (AMS)
- Established integrations with various other systems such as PRICES, HCAS PRISM, FBIS, and DocuSign



![This diagram illustrates the integration between automation, procurement, and reporting tools within the WorkSmarter ecosystem, emphasizing modularity and flow.](/Users/melissajackson/Documents/WorkSmarter Ecosystem Guide Project/Images/WorkSmarter Ecosystem Diagram.png)

### Figure 1: WorkSmarter Ecosystem Diagram



## Integrations

### PRICES

The PSC Revenue, Invoicing, and Cost Estimation System (PRICES) is the primary system used by the PSC & OS Service and Supply Fund activities to record customer agreements and corresponding financial project records, prepare and deliver customer invoices, and report on reimbursable activities.

### HCAS PRISM

HHS Consolidated Acquisition Solution (HCAS) is a financial system used by HHS Office of the Assistant Secretary for Financial Resources (ASFR) for federal procurement activities. This solution comprises the PRISM contract writing system and the Unified Financial Management System (UFMS). PRISM includes data regarding HHS statements of work, purchase requests, requests for proposals and quotes (RFPs/RFQs), bids, proposals, vendor invoices, requisitions, contract awards, contract modifications, progress reports, financial status reports, audit reports, and contract deliverables. Data is shared between PRISM and UFMS, completing the Procure to Pay (P2P) process

### FBIS

The Financial Business Information System (FBIS) is a reporting repository that pulls in data from various financial systems and allows people to run pre-made reports or create their own.

Reports that exist in FBIS are scheduled to be sent to WorkSmarter via email on a regular basis. WorkSmarter ingests these reports and uses the data in various applications. Because these reports are ingested by the platform as a whole, their data can be made available to any applications that reside on the platform. For example, invoice data from PRICES is used in ARS, CAM, and the ResourceFlow applications. See below for more information about each of these systems.

### DocuSign

DocuSign is a cloud-based SaaS platform used for electronic signatures and automating document workflows. It enables individuals and businesses to securely sign, send, and manage agreements digitally, replacing traditional paper-based processes.

In WorkSmarter, DocuSign is used primarily by the Customer Agreement Module to collect signatures on both non-Intrafund agreement orders and Intrafund agreements.

### AMS

The Access Management System (AMS) is the primary user authentication portal used to access computer systems and software applications at the U.S. Department of Health and Human Services (HHS). AMS protects applications owned directly by the Office of the Secretary and those that are owned and managed by various Operating Divisions.

WorkSmarter uses AMS to allow users to access the platform. A user must use either the HSPD-12 Access Card method or the AMS Credentials method to log into the platform and to use the applications. If using AMS Credentials, the user will also be required to use a One-Time Password (OTP) to satisfy multifactor authentication (MFA) requirements.



## Platform-wide Utilities

### Help Desk

The platform includes a custom field help desk ticketing utility that can be configured for use by individual teams that support different applications. For example, the PRISM and ARS Help Desk (part of the Office of Acquisition Management Services) uses this module to track and report on help desk activities pertaining to PRISM and ARS support, while the WorkSmarter Help Desk uses this module while supporting the other WorkSmarter applications. The application can be customized to capture team-specific data and integrate with the various applications on the platform.

### Knowledge Gateway

WorkSmarter has a Knowledge Gateway. It is the centralized point for access to information, resources, and expertise. It provides users with guides, training materials, videos, standard operating procedures (SOP), playing a crucial role in streamlining workflows, improving decision-making, and enhancing productivity by ensuring that relevant information is readily available to employees, IT teams, and stakeholders.



## Applications

### Acquisition Reporting System (ARS)

The Acquisition Reporting System is a tool used by acquisition staff within HHS to manage and streamline acquisition-related activities. ARS is designed to support the acquisition workforce (contract officers, contract specialists, program analysts) in managing and reporting on procurement activities, serving as a centralized platform to tracking, reporting, and storing acquisition-related data, which ensures consistency and compliance with federal acquisitions and HHS policies. These reports help HHS monitor procurement performance, ensure transparency, and meet federal reporting requirements (e.g., for Federal Procurement Data System (FPDS)).

### Customer Agreement Module (CAM)

The Customer Agreement Module streamlines data entry, agreement tracking, and billing processes for the Program Support Center (PSC). It serves as a centralized repository for all Interagency Agreement (IAA) data involving Service and Supply Fund (SSF) members, where the SSF member acts as the servicing agency.

CAM supports multiple agreement types, including:

- Orders processed through G-Invoicing

- Service Level Agreements (SLAs) managed in PRICES

- Intrafund agreements between two SSF member activities

- Non-Intrafund agreements documented via 7600A and 7600B forms

### ResourceFlow Formulation/Execution

The ResourceFlow is an application that standardizes the formulation and tracking of budgets within the SSF and is comprised two distinct modules: Formulation and Execution. Formulation creates budgets for the fiscal year two years into the future, and Execution is used for monitoring the current budget, create projections of costs and revenues, and report on operations. 

### Unified Dynamic Case Management (UDCM)

The Unified Dynamic Case Management application is a case-management application that standardizes the functions of the PSC portfolios and Human Resources (HR), including processes such as budget memos, purchase cards, board for corrections, and HR actions. Users can create customizable approval workflows for each case type, using these approvals to generate and fill-in HHS required forms, such as the HHS-755 purchase card approval request form.

### Position Description Management (PDM)

The Position Description Management application maintains accurate and up-to-date records of PSC employee position descriptions, positions, and hiring actions.

### Workflow Automation

The Workflow Automation system hosts several Robotic Process Automation (RPA) “bots”, which are automated workers that fulfill a specific operational need. RPA bots are primarily used to automate repetitive, routine tasks, increasing speed and accuracy. Examples of bots in use on the WorkSmarter platform include the ACF Grantee Intake bot, which is used to download hundreds of files from a SmartSheet based system, rename them, and transfer them to a receiving system; as well as the Security Manager Profile Bot, which receives data from the Smart Card Management System (SCMS) and uses that data to update employee profile information in the SecurityManager application. Automating these tasks improves speed (robots do not get tired or distracted) and data accuracy (robots do not make typos, miss data entry fields, or enter data inaccurately). At the same time, staff is freed up and available to undertake more high-value, high-thought activities.

The following RPA bots are currently operating on the WorkSmarter platform:

| RPA BOTS                                                | OPERATION                                                    |
| ------------------------------------------------------- | ------------------------------------------------------------ |
| Post-Payment Audit Processing                           | The PPA bot is used to review travel records in the ConcurGov system to validate that travel voucher amounts match their authorizations and receipts. |
| Contract Closeout Initiation                            | The CCI bot is used to automate the process to closeout federal acquisition contract actions (awards) in the HHS Consolidated Acquisition Solution (HCAS) PRISM system. If awards require modification before closeout, the bot creates the modification which is then completed by the appropriate contract officer. |
| Fingerprint SAC Bot                                     | The Fingerprint Special Agreement Check (SAC) bot connects to the SecurityManager system and downloads two reports, which are then uploaded into PSC's BITS/Locator system. |
| Administration for Children & Families (ACF) Intake Bot | The objective of the Program Support Center Administration for Children & Families (PSC ACF) Robotic Process Automation (RPA) for Emergency Intake Sites (EIS) Document Management is to support two document management functions: 1. ACF EIS document download from Smartsheet to a shared Network Drive for the Intake, Suitability, and Badging Service (ISBS) processing<br>2. Transferring the documents to a secured file location Business Intelligence Information System (BIIS-C) Dropbox to be consumed by SecurityManager. This will enable PSC staff to assist ACF with the efficient in-processing of contract staff from the Office of Refugee Resettlement (ORR) Division of Children’s Services (DCS) while maintaining compliance with federal requirements |
| SecurityManager Profile Bot                             | The objective of the Security Manager Profile Bot is to support the Program Support Center (PSC) onboarding efforts and reduce manual task repetition related to onboarding new staff. This is accomplished by enabling a Bot to function as a human by logging into Security Manager using its own login information and entering data into profiles from a report obtained from Smart Card Management System (SCMS). This process allows the PSC Intake, Suitability, and Badging Service (ISBS) staff to reduce manual workload in the onboarding process while maintaining compliance with federal requirements. |
| ACF Grantee Induction Bot                               | The objective of the Grantee Induction Robotic Process Automation (RPA) is to support two document management functions: <br/>1. Administration for Children and Families (ACF) document download from Smartsheet to a shared Network Drive for Intake, Suitability, and Badging Service (ISBS) processing<br/>2. Transferring the documents to a secured file location (Business Intelligence Information System Cloud (BIIS-C) Dropbox) to be consumed by SecurityManager. This will enable PSC staff to assist ACF with the efficient in-processing of grantees while maintaining compliance with federal requirements |
| USA Staffing File Import Bot                            | The USA Staffing File import Bot uses robotic process automation to call a Gateway Application Programming Interface (API) to download a list of federal employee badge and investigation applications for new hires. It will then log in to USA Staffing to download available applicant files and save the files in a zip file on the PSC Intake, Suitability, and Badging Services (ISBS) Network Drive. The Bot will then call a different Gateway API to push the applicant files to OneView. |



## Questions

As always, if you have any questions or concerns regarding the PSC WorkSmarter Ecosystem or WorkSmarter, please contact the WorkSmarter Help Desk at (555) 555-4555.
