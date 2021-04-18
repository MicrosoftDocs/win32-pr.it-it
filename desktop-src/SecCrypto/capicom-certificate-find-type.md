---
description: Il \_ \_ \_ tipo di enumerazione del tipo di individuazione del certificato di CAPICOM definisce il tipo di criteri di ricerca usati per trovare certificati specifici. Questo tipo di enumerazione è stato introdotto in capicol 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Enumerazione CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
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
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325164"
---
# <a name="capicom_certificate_find_type-enumeration"></a>\_Enumerazione del tipo di ricerca del certificato CApicol \_ \_

Il tipo di enumerazione del tipo di individuazione del certificato di CAPICOM definisce il tipo di criteri di ricerca usati per trovare certificati specifici. **\_ \_ \_** Questo tipo di enumerazione è stato introdotto in capicol 2,0.

## <a name="members"></a>Membri



| Membro                                                | Descrizione                                                                                                                                 | Valore |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Il certificato CAPICOM \_ \_ trova \_ hash SHA1 \_**            | Restituisce i certificati corrispondenti a un hash SHA1 specificato.<br/>                                                                             | 0     |
| **\_ \_ \_ nome oggetto trovato certificato capicot \_**         | Restituisce i certificati il cui nome soggetto è esattamente o parzialmente corrispondente a un nome soggetto specificato.<br/>                                   | 1     |
| **\_ \_ \_ nome dell'autorità emittente trovare il certificato di CAPICOM \_**          | Restituisce i certificati il cui nome dell'autorità di certificazione corrisponde esattamente o parzialmente a un nome di autorità emittente specificato.<br/>                                     | 2     |
| **\_ \_ \_ nome radice trovato certificato capicol \_**            | Restituisce i certificati il cui nome soggetto radice corrisponde esattamente o parzialmente a un nome soggetto radice specificato.<br/>                         | 3     |
| **\_nome del modello di \_ ricerca del certificato \_ CAPICOM \_**        | Restituisce i certificati il cui nome modello corrisponde a un nome di modello specificato.<br/>                                                      | 4     |
| **estensione per la \_ ricerca del certificato CApicol \_ \_**             | Restituisce i certificati con un'estensione che corrisponde a un'estensione specificata.<br/>                                                  | 5     |
| **il certificato CAPICOM \_ \_ trova la \_ \_ proprietà estesa**    | Restituisce i certificati che dispongono di una proprietà estesa il cui identificatore di proprietà corrisponde a un identificatore di proprietà specificato.<br/>           | 6     |
| **\_ \_ criterio di ricerca \_ dell'applicazione \_ per il certificato capicol**   | Restituisce i certificati nell'archivio che dispongono di una proprietà o di un'estensione di utilizzo chiavi avanzata combinata a un identificatore di utilizzo.<br/> | 7     |
| **\_ \_ criterio di individuazione \_ \_ certificati di capicol**   | Restituisce i certificati contenenti un OID di criteri specificato.<br/>                                                                          | 8     |
| **tempo di ricerca certificato capicol \_ \_ \_ \_ valido**           | Restituisce i certificati il cui tempo è valido.<br/>                                                                                        | 9     |
| **tempo di individuazione del certificato capicol \_ \_ \_ \_ non \_ ancora \_ valido** | Restituisce i certificati il cui tempo non è ancora valido.<br/>                                                                                | 10    |
| **tempo di individuazione certificato capicot \_ \_ \_ \_ scaduto**         | Restituisce i certificati il cui tempo è scaduto.<br/>                                                                                     | 11    |
| **\_ \_ utilizzo chiave di ricerca del certificato CAPICOM \_ \_**            | Restituisce i certificati contenenti una chiave che può essere utilizzata nel modo specificato.<br/>                                                  | 12    |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione del **\_ tipo di \_ individuazione \_ del certificato CAPICOM** viene utilizzato dal metodo [**Certificates. Find**](certificates-find.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




