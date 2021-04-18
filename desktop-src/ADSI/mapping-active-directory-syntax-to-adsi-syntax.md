---
title: Mapping della sintassi di Active Directory alla sintassi ADSI
description: Nella tabella seguente viene eseguito il mapping della sintassi Active Directory alle relative sintassi ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- attributi ADSI, mapping Active Directory sintassi alla sintassi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297667"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Mapping della sintassi di Active Directory alla sintassi ADSI

Nella tabella seguente viene eseguito il mapping della sintassi Active Directory alle relative sintassi ADSI.



| ID sintassi attributo | Tipo di sintassi Active Directory             | Tipo di sintassi ADSI equivalente                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Stringa DN<br/>                     | Stringa DN<br/>                                                |
| 2.5.5.2<br/>  | ID dell'oggetto.<br/>                     | Stringa CaseIgnore<br/>                                        |
| 2.5.5.3<br/>  | Stringa distinzione tra maiuscole e minuscole<br/>         | Stringa CaseExact<br/>                                         |
| 2.5.5.4<br/>  | Stringa case ignorata<br/>           | Stringa CaseIgnore<br/>                                        |
| 2.5.5.5<br/>  | Stringa del case di stampa<br/>             | Stringa stampabile<br/>                                         |
| 2.5.5.6<br/>  | Stringa numerica<br/>                | Stringa numerica<br/>                                           |
| 2.5.5.7<br/>  | **O** Nome DNWithOctetString<br/> | Non supportato<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Integer<br/>                       | Integer<br/>                                                  |
| 2.5.5.10<br/> | Stringa ottetto<br/>                  | Stringa ottetto<br/>                                             |
| 2.5.5.11<br/> | Tempo<br/>                          | Ora UTC<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Stringa Case Ignore<br/>                                       |
| 2.5.5.13<br/> | Indirizzo<br/>                       | Non supportato<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Descrittore di sicurezza NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Integer grande<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Stringa ottetto<br/>                                             |



 

 

 





