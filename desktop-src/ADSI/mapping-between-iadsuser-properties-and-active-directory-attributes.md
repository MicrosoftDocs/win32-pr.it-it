---
title: Mapping tra le proprietà di IADsUser e gli attributi di Active Directory
description: Se applicabile, viene eseguito il mapping di una proprietà dell'oggetto utente ADSI a un attributo Active Directory appropriato. Le proprietà dell'oggetto utente ADSI sono associate ai metodi della proprietà IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Mapping tra le proprietà IADsUser e gli attributi Active Directory ADSI
- ADSI del provider LDAP, oggetto utente, mapping tra le proprietà di IADsUser e gli attributi di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b817a8c56e2c74c846e1343e0ed7803427f4a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399722"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Mapping tra le proprietà di IADsUser e gli attributi di Active Directory

Se applicabile, viene eseguito il mapping di una proprietà dell'oggetto utente ADSI a un attributo Active Directory appropriato. Le proprietà dell'oggetto utente ADSI sono associate ai metodi della proprietà [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

Nella tabella seguente viene elencato il mapping tra le proprietà di [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) per il provider LDAP e l'attributo Active Directory corrispondente.



| Proprietà IADsUser                                           | Attributo Active Directory                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **Annunci \_ Flag UF \_ ACCOUNTDISABLE** nell'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Non supportato.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Reparto**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Descrizione**](iadsuser-property-methods.md)            | [**Descrizione**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Divisione**](iadsuser-property-methods.md)               | [**Divisione**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**posta elettronica**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**EmployeeID**](iadsuser-property-methods.md)             | [**employeeID**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**NumeroFax**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**displayName**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Non supportato.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Non supportato.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Home page**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Linguaggi**](iadsuser-property-methods.md)              | Non supportato.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**sn**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Manager**](iadsuser-property-methods.md)                | [**manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | Non supportato.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**UPN**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Imposta usando Criteri di gruppo editor                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Imposta usando Criteri di gruppo editor                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **Annunci \_ Flag \_ \_ NOTREQD di UF passwd** nell'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) . |
| [**Immagine**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**PostalCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Profilo**](iadsuser-property-methods.md)                | [**PercorsoProfilo**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Imposta usando Criteri di gruppo editor                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**mobili**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**pager**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Titolo**](iadsuser-property-methods.md)                  | [**titolo**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 