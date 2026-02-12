# ACF-ORR Web API



## Table of Contents

- [Background](#background)
- [User Access](#user-access)
- [Connection Requirements](#connection-requirements)
- [Data Parameters](#data-parameters)
- [Response](#response)



## Background

This web API was created for ACF to call via their Tableau instance to pull data from the ACF/ORR dashboard hosted on PSC's WorkSmarter platform.

## User Access

The web API uses OAuth2.0 connection. Therefore, users must create an integration of type OAuth 2.0 on their end.

## Connection Requirements

| web API                | OAuth 2.0                                                    |
| ---------------------- | ------------------------------------------------------------ |
| Client ID              | This information will be provided to the client by the WorkSmarter team when your access is established. |
| Client Secret          | This information will be provided to the client by the WorkSmarter team when your access is established |
| Token Request Endpoint | - **Production:** https://worksmarter.appiancloud.us/suite/authorization/oauth/token  <br/>- **Test:** https://worksmartertest.appiancloud.us/suite/authorization/oauth/token  <br/>- **Development:** https://worksmarterdev.appiancloud.us/suite/authorization/oauth/token  <br/>- **Staging:** https://worksmarterstage.appiancloud.us/suite/authorization/oauth/token |
| Endpoint URL           | - **Production:** https://worksmarter.appiancloud.us/suite/webapi/getACF-ORRGranteeRecords  <br/>- **Test:** https://worksmartertest.appiancloud.us/suite/webapi/getACF-ORRGranteeRecords  <br/>- **Development:** https://worksmarterdev.appiancloud.us/suite/webapi/getACF-ORRGranteeRecords  <br/>- **Staging:** https://worksmarterstage.appiancloud.us/suite/webapi/getACF-ORRGranteeRecords |

## Data Parameters

| Parameter Name | Type    | Required | Request Type | Notes                                                        |
| -------------- | ------- | -------- | ------------ | ------------------------------------------------------------ |
| startindex     | integer | Yes      | GET          | Due to size limitations, the calling application may need to make multiple calls to the API to retrieve all records. The startindex field will be used to indicate which record to start with while called via loop. |
| batchSize      | integer | Yes      | GET          | The number of records to return in each pull. The maximum size is currently 1000 records. |

## Response

| Field Name             | Data Type | Potential Number of Elements | Report                                                       |
| ---------------------- | --------- | ---------------------------- | ------------------------------------------------------------ |
| id                     | Number    | One                          |                                                              |
| hhsId                  | String    | One                          | ACF Bulk Load Status Report <br>ACF ORR Status (Incomplete) <br>ACF ORR Status (Complete) |
| ssn                    | String    | One                          | ACF Bulk Load Status Report <br>ACF IRA Case Details         |
| lastName               | Text      | One                          | ACF Bulk Load Status Report <br>ACF ORR Status (Incomplete)  |
| firstName              | Text      | One                          | ACF Bulk Load Status Report <br/>ACF ORR Status (Incomplete) <br/>ACF ORR Status (Complete) |
| middleName             | Text      | One                          | ACF Bulk Load Status Report                                  |
| email                  | Text      | One                          | ACF Bulk Load Status Report                                  |
| agency                 | Text      | One                          | ACF Bulk Load Status Report                                  |
| subAgency              | Text      | One                          | ACF Bulk Load Status Report                                  |
| division               | Text      | One                          | ACF Bulk Load Status Report                                  |
| contractName           | Text      | One                          | ACF Bulk Load Status Report                                  |
| eisLocation            | Text      | One                          | ACF Bulk Load Status Report                                  |
| eisState               | Text      | One                          | ACF Bulk Load Status Report                                  |
| applicationCreated     | String    | One                          | ACF Bulk Load Status Report                                  |
| invType                | String    | One                          | ACF Bulk Load Status Report                                  |
| eAppInitiated          | String    | One                          | ACF Bulk Load Status Report                                  |
| eAppInitiated2         | Text      | One                          | ACF Bulk Load Status Report                                  |
| eAppInitiated3         | Text      | One                          | ACF Bulk Load Status Report                                  |
| invAdjudicationDate    | Text      | One                          | ACF Bulk Load Status Report                                  |
| invAdjudicationResults | Text      | One                          | ACF Bulk Load Status Report                                  |
| invStatus              | Text      | One                          | ACF Bulk Load Status Report                                  |
| invStatusDate          | String    | One                          | ACF Bulk Load Status Report                                  |
| fpStatus               | Text      | One                          | ACF Bulk Load Status Report                                  |
| fpStatusDate           | Text      | One                          | ACF Bulk Load Status Report                                  |
| fpAdjResult            | Text      | One                          | ACF Bulk Load Status Report                                  |
| of306Status            | Text      | One                          | ACF Bulk Load Status Report                                  |
| of306StatusDate        | Text      | One                          | ACF Bulk Load Status Report                                  |
| eqipApplicantName      | Text      | One                          | Eqip Report                                                  |
| eqipStatus             | Text      | One                          | Eqip Report                                                  |
| eqipCaseType           | Text      | One                          | Eqip Report                                                  |
| eqipLastAction         | Text      | One                          | Eqip Report                                                  |
| eqipDateInitiated      | Text      | One                          | Eqip Report                                                  |
| emailedDate            | String    | One                          | ACF ORR Status (Incomplete) <br>ACF ORR Status (Complete)    |
| loggedIn               | Text      | One                          | ACF ORR Status (Incomplete);                                 |
| appointmentDate        | Date      | One                          | ACF ORR Status (Incomplete) <br>ACF ORR Status (Complete)    |
| enrolledDate           | String    | One                          | ACF ORR Status (Incomplete) <br/>ACF ORR Status (Complete)   |
| formRoutingName        | Text      | One                          | ACF IRA Case Details                                         |
| initiatorOrgName       | Text      | One                          | ACF IRA Case Details                                         |
| caseId                 | String    | One                          | ACF IRA Case Details                                         |
| caseInitiatedDate      | Date      | One                          | ACF IRA Case Details                                         |
| caseExpirationDate     | Date      | One                          | ACF IRA Case Details                                         |
| daysUntilExpired       | Number    | One                          | ACF IRA Case Details                                         |
| sfDateReceived         | Date      | One                          | ACF IRA Case Details                                         |
| sfDateSubmitted        | Date      | One                          | ACF IRA Case Details                                         |
| caseType               | String    | One                          | ACF IRA Case Details <br>ACF e-QIP                           |
| caseStatus             | Text      | One                          | ACF IRA Case Details                                         |
| affiliation            | Text      | One                          | ACF IRA Case Details                                         |
| formType               | String    | One                          | ACF IRA Case Details                                         |
| subjectEmail           | Text      | One                          | ACF IRA Case Details                                         |
| subjectLastName        | Text      | One                          | ACF IRA Case Details                                         |
| subjectFirstName       | Text      | One                          | ACF IRA Case Details                                         |
| dob                    | String    | One                          | ACF IRA Case Details                                         |
| affiliationCategory    | Text      | One                          | ACF IRA Case Details                                         |
| subjectPortalLoginId   | String    | One                          | ACF IRA Case Details                                         |
| sensitivity            | Text      | One                          | ACF IRA Case Details                                         |
| risk                   | Text      | One                          | ACF IRA Case Details                                         |
| createdBy              | Text      | One                          |                                                              |
| createdDate            | String    | One                          |                                                              |
| updatedBy              | Text      | One                          |                                                              |
| updatedDate            | Text      | One                          |                                                              |

**if batch size exceeds 1000**

| Field Name   | Data Type | Potential Number of Elements |
| ------------ | --------- | ---------------------------- |
| errorCode    | Number    | One                          |
| errorMessage | Text      | One                          |

**Data Sample (startindex)**

```
[

  {

​    "id": 1,

​    "hhsId": "2002114425",

​    "ssn": "000-00-0000",

​    "lastName": "LUIGI",

​    "firstName": "JOHN",

​    "middleName": "MARIO",

​    "email": "JOHN.LUIGI@SAMHSA.HHS.GOV",

​    "agency": "ACF",

​    "subAgency": "ORR",

​    "division": "Grant",

​    "contractName": "Bethany HSPRS",

​    "eisLocation": "",

​    "eisState": "",

​    "applicationCreated": "2024-10-22T00:00:00Z",

​    "invType": "Tier 1",

​    "eAppInitiated": "2024-10-22T00:00:00Z",

​    "eAppInitiated2": `null`,

​    "eAppInitiated3": `null`,

​    "invAdjudicationDate": `null`,

​    "invAdjudicationResults": "",

​    "invStatus": "Initiated",

​    "invStatusDate": "2024-10-22T00:00:00Z",

​    "fpStatus": "",

​    "fpStatusDate": `null`,

​    "fpAdjResult": "",

​    "of306Status": "",

​    "of306StatusDate": `null`,

​    "eqipApplicantName": `null`,

​    "eqipStatus": `null`,

​    "eqipCaseType": `null`,

​    "eqipLastAction": `null`,

​    "eqipDateInitiated": `null`,

​    "emailedDate": "2024-10-21T10:17:06Z",

​    "loggedIn": "NEVER",

​    "appointmentDate": `null`,

​    "enrolledDate": "2016-07-27T00:00:00Z",

​    "formRoutingName": "PSC ISBS SUITABILITY",

​    "initiatorOrgName": "ACF GRANTEES",

​    "caseId": "24296CHIC0842571",

​    "caseInitiatedDate": "2024-10-22",

​    "caseExpirationDate": "2025-01-25",

​    "daysUntilExpired": 87,

​    "sfDateReceived": `null`,

​    "sfDateSubmitted": `null`,

​    "caseType": "Tier 1",

​    "caseStatus": "Applicant Editing Form",

​    "affiliation": "Contractor",

​    "formType": "SF85",

​    "subjectEmail": "johnchica@bethany.org",

​    "subjectLastName": "Luigi",

​    "subjectFirstName": "John",

​    "dob": "2066-05-31Z",

​    "affiliationCategory": "CON",

​    "subjectPortalLoginId": "jchi746483",

​    "sensitivity": "Non-Sensitive",

​    "risk": "Low Risk",

​    "createdBy": "vyjanya.dasari@psc.hhs.gov",

​    "createdDate": "2025-03-10T15:36:31Z",

​    "updatedBy": `null`,

​    "updatedDate": `null`

  },
```



**if batchSize exceeds 1000**

```
 {

  "errorCode": 1,

  "errorMessage": "batch size too high"

}
```