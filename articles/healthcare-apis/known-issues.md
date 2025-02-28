---
title: Azure Health Data Services known issues
description: This article provides details about the known issues of Azure Health Data Services.
services: healthcare-apis
author: kgaddam10
ms.service: healthcare-apis
ms.subservice: fhir
ms.topic: reference
ms.date: 06/07/2022
ms.author: mikaelw
---

# Known issues: Azure Health Data Services

This article describes the currently known issues with Azure Health Data Services and its different service types (FHIR service, DICOM service, and MedTech service) that seamlessly work with one another.

Refer to the table below to find details about resolution dates or possible workarounds. For more information about the different feature enhancements and bug fixes in Azure Health Data Services, see [Release notes: Azure Health Data Services](release-notes.md).

## FHIR service

|Issue | Date discovered | Workaround | Date resolved |
| :------------------------------------- | :------------ | :------------- | :------------- |
|Using [token type](https://www.hl7.org/fhir/search.html#token) fields of length more than 128 characters can result in undesired behavior on `create`, `search`, `update`, and `delete` operations.  | August 2022  |No workaround  | Not resolved |
|The SQL provider will cause the `RawResource` column in the database to save incorrectly. This occurs in a small number of cases when a transient exception occurs that causes the provider to use its retry logic. |April 2022 |-|May 2022 Resolved [#2571](https://github.com/microsoft/fhir-server/pull/2571) |
| Queries not providing consistent result counts after appended with `_sort` operator. For more information, see [#2680](https://github.com/microsoft/fhir-server/pull/2680). | July 2022 | No workaround|August 2022 Resolved |

## Next steps

In this article, you learned about the currently known issues with Azure Health Data Services. For more information about Azure Health Data Services, see

>[!div class="nextstepaction"]
>[About Azure Health Data Services](healthcare-apis-overview.md)

For information about the features and bug fixes in Azure API for FHIR, see

>[!div class="nextstepaction"]
>[Release notes: Azure API for FHIR](./azure-api-for-fhir/release-notes.md)

FHIR&#174; is a registered trademark of [HL7](https://hl7.org/fhir/) and is used with the permission of HL7. 