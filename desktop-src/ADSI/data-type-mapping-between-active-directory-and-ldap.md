---
title: Mapping dei tipi di dati tra Active Directory e LDAP
description: Nella tabella seguente viene eseguito il mapping del nome descrittivo della sintassi per l'OID e il valore ADSTYPEENUM della sintassi LDAP corrispondente.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- mapping dei tipi di dati tra Active Directory e LDAP ADSI
- ADSI del provider di servizi LDAP, mapping dei tipi di dati tra Active Directory e LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45157fb7cefe1a993e6e16dffe28f101bc73759b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297690"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Mapping dei tipi di dati tra Active Directory e LDAP

Nella tabella seguente viene eseguito il mapping del nome descrittivo della sintassi per l'OID e il valore [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) della sintassi LDAP corrispondente.



| Nome descrittivo della sintassi              | OID sintassi LDAP               | Tipo di dati ADSTYPEENUM                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| Audio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **\_stringa ottetto \_ ADSTYPE**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **\_stringa ottetto \_ ADSTYPE**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE ( \_ booleano)**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **\_ \_ stringa esatta del case ADSTYPE \_**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| Certificato                       | 1.3.6.1.4.1.1466.115.121.1.8  | **\_stringa ottetto \_ ADSTYPE**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **\_stringa ottetto \_ ADSTYPE**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **\_stringa ottetto \_ ADSTYPE**            |
| Paese/Area geografica                    | 1.3.6.1.4.1.1466.115.121.1.11 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| DirectoryString                   | 1.3.6.1.4.1.1466.115.121.1.15 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **\_stringa DN \_ ADSTYPE**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **\_stringa ottetto \_ ADSTYPE**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ \_ ora UTC**                |
| Ora (solo il server del sito esegue questa operazione) | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ \_ ora UTC**                |
| Guida                             | 1.3.6.1.4.1.1466.115.121.1.25 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **ADSTYPE \_ Integer**                  |
| INTEGER8 (non in LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **ADSTYPE \_ \_ Integer grande**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **\_stringa ottetto \_ ADSTYPE**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **\_stringa numerica ADSTYPE \_**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| OctetString (non in RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **\_stringa ottetto \_ ADSTYPE**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **\_stringa stampabile \_ ADSTYPE**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **\_descrittore di sicurezza NT ADSTYPE \_ \_** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **\_stringa ottetto \_ ADSTYPE**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **ADSTYPE \_ case \_ Ignora \_ stringa**     |
| UTCTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **ADSTYPE \_ \_ ora UTC**                |



 

 

 




