---
description: Usato con il metodo Store.Open per indicare come deve essere aperto un archivio certificati.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: CAPICOM_STORE_OPEN_MODE enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ebd46b751f4a098361618f3b6e992e4333425f501bf6afdedfca047e921ad7ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772058"
---
# <a name="capicom_store_open_mode-enumeration"></a>Enumerazione CAPICOM \_ STORE \_ OPEN \_ MODE

Il tipo di enumerazione CAPICOM STORE OPEN MODE viene usato con il metodo \_ \_ \_ [**Store.Open**](store-open.md) per indicare la modalità di apertura di un archivio certificati.

## <a name="members"></a>Membri



| Membro                                      | Descrizione                                                                                                                                                              | Valore |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY**        | Aprire l'archivio in modalità di sola lettura.<br/>                                                                                                                             | 0     |
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**       | Aprire l'archivio in modalità lettura/scrittura.<br/>                                                                                                                            | 1     |
| **CAPICOM \_ STORE OPEN MAXIMUM ALLOWED (APERTURA MASSIMA CONSENTITA PER CAPICOM \_ \_ \_ STORE)**  | Aprire l'archivio in modalità lettura/scrittura se l'utente dispone delle autorizzazioni di lettura/scrittura. Se l'utente non dispone di autorizzazioni di lettura/scrittura, aprire l'archivio in modalità di sola lettura.<br/> | 2     |
| **CAPICOM \_ STORE OPEN EXISTING ONLY \_ \_ (APRI SOLO \_ ESISTENTE)**    | Aprire solo gli archivi esistenti; non creare un nuovo archivio. Introdotto da CAPICOM 2.0.<br/>                                                                              | 128   |
| **CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED** | Includere i certificati archiviati quando si usa l'archivio. Introdotto da CAPICOM 2.0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Commenti

Quando si usa l'enumerazione CAPICOM STORE OPEN MODE, è possibile usare solo \_ \_ una delle impostazioni \_ seguenti.

-   CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY
-   CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE
-   CAPICOM \_ STORE OPEN MAXIMUM ALLOWED (APERTURA MASSIMA CONSENTITA PER CAPICOM \_ \_ \_ STORE)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store.Open**](store-open.md)
</dt> </dl>

 

 




