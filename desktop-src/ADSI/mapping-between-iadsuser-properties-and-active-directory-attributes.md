---
title: Mapping tra le proprietà IADsUser e gli attributi di Active Directory
description: Se applicabile, viene eseguito il mapping di una proprietà dell'oggetto utente ADSI a un attributo di Active Directory appropriato. Le proprietà dell'oggetto utente ADSI sono associate ai metodi della proprietà IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Mapping tra le proprietà IADsUser e gli attributi di Active Directory ADSI
- Provider LDAP ADSI, oggetto utente, mapping tra proprietà IADsUser e attributi di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e659c6325457b2654ad5cfeef964975949150232c4ae3376fac640c51c41aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839481"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Mapping tra le proprietà IADsUser e gli attributi di Active Directory

Se applicabile, viene eseguito il mapping di una proprietà dell'oggetto utente ADSI a un attributo di Active Directory appropriato. Le proprietà dell'oggetto utente ADSI sono associate ai metodi della proprietà [**IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser)

La tabella seguente elenca il mapping tra le [**proprietà IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) per il provider LDAP e l'attributo Active Directory corrispondente.



| IADsUser - proprietà                                           | Attributo di Active Directory                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **Servizi di dominio Active Directory \_ Flag \_ UF ACCOUNTDISABLE** [**nell'attributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | Non supportato.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Dipartimento**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Descrizione**](iadsuser-property-methods.md)            | [**description**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Divisione**](iadsuser-property-methods.md)               | [**Divisione**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**EmployeeID**](iadsuser-property-methods.md)             | [**Employeeid**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**Numero fax**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**Fullname**](iadsuser-property-methods.md)               | [**displayName**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | Non supportato.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | Non supportato.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Homepage**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**Lockouttime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Linguaggi**](iadsuser-property-methods.md)              | Non supportato.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**sn**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Manager**](iadsuser-property-methods.md)                | [**Manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | Non supportato.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Impostare usando l Criteri di gruppo editor                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Impostare usando l Criteri di gruppo editor                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **Servizi di dominio Active Directory \_ Flag \_ \_ NOTREQD PASSWD UF** nell'attributo [**userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol) |
| [**Immagine**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**Codici postali**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Profilo**](iadsuser-property-methods.md)                | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Impostare usando l Criteri di gruppo editor                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelefonoHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelefonoMobile**](iadsuser-property-methods.md)        | [**Mobile**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**Numero di telefono**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Titolo**](iadsuser-property-methods.md)                  | [**Titolo**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 