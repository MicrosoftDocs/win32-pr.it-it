---
title: Mapping della sintassi di Active Directory alla sintassi ADSI
description: Nella tabella seguente viene eseguito il mapping delle sintassi di Active Directory alle sintassi ADSI corrispondenti.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- attributi ADSI, mapping della sintassi di Active Directory alla sintassi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04682a1e299e14c55c520310bff697ea6664d4dabe71380f7a146fd2dfff053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179279"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Mapping della sintassi di Active Directory alla sintassi ADSI

Nella tabella seguente viene eseguito il mapping delle sintassi di Active Directory alle sintassi ADSI corrispondenti.



| ID sintassi dell'attributo | Tipo di sintassi Active Directory             | Tipo di sintassi ADSI equivalente                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Stringa DN<br/>                     | Stringa DN<br/>                                                |
| 2.5.5.2<br/>  | ID dell'oggetto.<br/>                     | Stringa CaseIgnore<br/>                                        |
| 2.5.5.3<br/>  | Stringa con distinzione tra maiuscole e minuscole<br/>         | Stringa CaseExact<br/>                                         |
| 2.5.5.4<br/>  | Stringa ignorata maiuscole/minuscole<br/>           | Stringa CaseIgnore<br/>                                        |
| 2.5.5.5<br/>  | Stampa stringa maiuscole/minuscole<br/>             | Stringa stampabile<br/>                                         |
| 2.5.5.6<br/>  | Stringa numerica<br/>                | Stringa numerica<br/>                                           |
| 2.5.5.7<br/>  | **OR** Nome DNWithOctetString<br/> | Non supportato<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Intero<br/>                       | Intero<br/>                                                  |
| 2.5.5.10<br/> | Octet String<br/>                  | Octet String<br/>                                             |
| 2.5.5.11<br/> | Ora<br/>                          | Ora UTC<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Stringa ignorata maiuscole/minuscole<br/>                                       |
| 2.5.5.13<br/> | Indirizzo<br/>                       | Non supportato<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Descrittore di sicurezza NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Large Integer<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Octet String<br/>                                             |



 

 

 





