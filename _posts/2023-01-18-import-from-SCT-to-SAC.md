---
title: Import Data from SCT to SAC
date: 2024-01-18  #YYYY-MM-DD HH:MM:SS +/-TTTT
last_modified_at : 2024-01-18
categories: ['TIL', 'SAP'] #[TOP_CATEGORIE, SUB_CATEGORIE]
tags: [gitblog, chirpy]     # TAG names should always be lowercase
#math: true

toc : true
toc_sticky : true
---


## Issue 
I wanted to import SCT(Sustainability Control Tower) data into SAC (SAP Analytics Cloud)

## What I've tried 
As SCT is based on PaPM, I tried ways to connect PaPM to SAC.
1. OData Connection (Ytable)
2. HANA table Connection


## Solution
HANA table Connection does not work because I do not have access to the information of the HANA DB of the SCT.

OData Connection did not work as it did in PaPM, but I was able to connect SCT OData API to SAC through OData Connection.


## Lesson Learned
Data from outbound APIs can be imported with OData Services Connection.
Fill in the following items.
Data Service URL : https://<span>xxxxxxxxxx/api/sct-analytics-service/v1/sustainabilityMetrics -> because I am using the API '[SustainabilityMetrics](https://api.sap.com/api/SustainabilityMetrics/overview)'
OAuth Client ID
Secret 
Token URL : add /oauth/token at the end.
<img width="355" alt="Screenshot 2024-01-18 at 7 41 51 PM" src="https://github.com/sjk521/sjk521.github.io/assets/31619869/562ff9cb-6129-4139-b239-0199228d0648">



## Maybe tomorrow
Understand how the connection works.
Understand what OData really means.