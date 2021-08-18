---
title: Mapping dei tipi di dati tra Active Directory e LDAP
description: Nella tabella seguente viene eseguito il mapping del nome descrittivo della sintassi al valore OID e ADSTYPEENUM della sintassi LDAP corrispondente.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- mapping dei tipi di dati tra Active Directory e LDAP ADSI
- Provider di servizi LDAP ADSI, mapping dei tipi di dati tra Active Directory e LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1aed0ff0071c55e381e1eb66f1f84e5a98aa8acf2c361816444533c6d0ad886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961970"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Mapping dei tipi di dati tra Active Directory e LDAP

Nella tabella seguente viene eseguito il mapping del nome descrittivo della sintassi al valore OID e [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) della sintassi LDAP corrispondente.



| Nome descrittivo della sintassi              | OID della sintassi LDAP               | Tipo di dati ADSTYPEENUM                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Audio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE \_ BOOLEAN**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **STRINGA ESATTA DEL CASE ADSTYPE \_ \_ \_**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Certificato                       | 1.3.6.1.4.1.1466.115.121.1.8  | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| Paese/Area geografica                    | 1.3.6.1.4.1.1466.115.121.1.11 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Metodo di recapito                    | 1.3.6.1.4.1.1466.115.121.1.14 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DirectoryString                   | 1.3.6.1.4.1.1466.115.121.1.15 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **STRINGA DN ADSTYPE \_ \_**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **ORA UTC ADSTYPE \_ \_**                |
| Ora (solo il server del sito esegue questa operazione) | 1.3.6.1.4.1.1466.115.121.1.24 | **ORA UTC ADSTYPE \_ \_**                |
| Guida                             | 1.3.6.1.4.1.1466.115.121.1.25 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **ADSTYPE \_ INTEGER**                  |
| INTEGER8 (non in LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **ADSTYPE \_ LARGE \_ INTEGER**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **STRINGA NUMERICA \_ ADSTYPE \_**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| OctetString (non in RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **STRINGA STAMPABILE ADSTYPE \_ \_**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **DESCRITTORE DI \_ SICUREZZA ADSTYPE NT \_ \_** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **STRINGA DELL'OTTETTO ADSTYPE \_ \_**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| UTCTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **ORA UTC ADSTYPE \_ \_**                |



 

 

 




