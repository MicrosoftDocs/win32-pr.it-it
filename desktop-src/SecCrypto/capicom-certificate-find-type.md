---
description: Il tipo di enumerazione \_ CAPICOM CERTIFICATE \_ FIND TYPE definisce il tipo di criteri di ricerca usati per trovare certificati \_ specifici. Questo tipo di enumerazione è stato introdotto in CAPICOM 2.0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: CAPICOM_CERTIFICATE_FIND_TYPE enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fb10b9289ae094f27fe29c3f2723d639eccc029aa7e5512833ac7e859c5c36ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772696"
---
# <a name="capicom_certificate_find_type-enumeration"></a>Enumerazione CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE

Il **tipo di enumerazione \_ CAPICOM CERTIFICATE FIND \_ \_ TYPE** definisce il tipo di criteri di ricerca usati per trovare certificati specifici. Questo tipo di enumerazione è stato introdotto in CAPICOM 2.0.

## <a name="members"></a>Membri



| Membro                                                | Descrizione                                                                                                                                 | Valore |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**            | Restituisce i certificati corrispondenti a un hash SHA1 specificato.<br/>                                                                             | 0     |
| **CAPICOM \_ CERTIFICATE FIND SUBJECT NAME (TROVA NOME SOGGETTO DEL CERTIFICATO CAPICOM) \_ \_ \_**         | Restituisce i certificati il cui nome soggetto corrisponde esattamente o parzialmente a un nome soggetto specificato.<br/>                                   | 1     |
| **CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME**          | Restituisce i certificati il cui nome dell'autorità di certificazione corrisponde esattamente o parzialmente a un nome di autorità emittente specificato.<br/>                                     | 2     |
| **TROVARE IL \_ NOME RADICE \_ DEL \_ CERTIFICATO \_ CAPICOM**            | Restituisce i certificati il cui nome soggetto radice corrisponde esattamente o parzialmente a un nome soggetto radice specificato.<br/>                         | 3     |
| **NOME MODELLO \_ DI RICERCA \_ CERTIFICATO \_ CAPICOM \_**        | Restituisce i certificati il cui nome di modello corrisponde a un nome di modello specificato.<br/>                                                      | 4     |
| **ESTENSIONE CAPICOM \_ CERTIFICATE \_ FIND \_**             | Restituisce i certificati con un'estensione che corrisponde a un'estensione specificata.<br/>                                                  | 5     |
| **PROPRIETÀ ESTESA \_ TROVA \_ CERTIFICATO \_ \_ CAPICOM**    | Restituisce i certificati con una proprietà estesa il cui identificatore di proprietà corrisponde a un identificatore di proprietà specificato.<br/>           | 6     |
| **CRITERI \_ DELL'APPLICAZIONE CAPICOM CERTIFICATE \_ FIND \_ \_**   | Restituisce i certificati nell'archivio con un'estensione per l'utilizzo chiavi avanzata o una proprietà combinata con un identificatore di utilizzo.<br/> | 7     |
| **CRITERI DI \_ RICERCA CERTIFICATI CAPICOM \_ \_ \_**   | Restituisce i certificati contenenti un OID dei criteri specificato.<br/>                                                                          | 8     |
| **ORA DI RICERCA CERTIFICATO CAPICOM \_ \_ \_ \_ VALIDA**           | Restituisce i certificati la cui ora è valida.<br/>                                                                                        | 9     |
| **ORA DI RICERCA DEL CERTIFICATO CAPICOM \_ \_ NON ANCORA \_ \_ \_ \_ VALIDA** | Restituisce i certificati la cui ora non è ancora valida.<br/>                                                                                | 10    |
| **TEMPO DI RICERCA CERTIFICATO CAPICOM \_ \_ \_ \_ SCADUTO**         | Restituisce i certificati il cui tempo è scaduto.<br/>                                                                                     | 11    |
| **INDIVIDUAZIONE \_ DELL'UTILIZZO \_ DELLA CHIAVE PER IL \_ CERTIFICATO \_ CAPICOM**            | Restituisce i certificati contenenti una chiave che può essere utilizzata nel modo specificato.<br/>                                                  | 12    |



## <a name="remarks"></a>Commenti

Il **tipo di enumerazione \_ CAPICOM CERTIFICATE FIND \_ \_ TYPE** viene usato dal [**metodo Certificates.Find.**](certificates-find.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




