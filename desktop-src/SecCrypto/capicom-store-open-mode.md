---
description: Utilizzato con il metodo Store. Open per indicare la modalità di apertura di un archivio certificati.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Enumerazione CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
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
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331049"
---
# <a name="capicom_store_open_mode-enumeration"></a>\_Enumerazione della modalità di apertura dell'archivio CAPICOM \_ \_

Il \_ \_ tipo di enumerazione di archivio CAPICOM \_ viene usato con il metodo [**Store. Open**](store-open.md) per indicare la modalità di apertura di un archivio certificati.

## <a name="members"></a>Membri



| Membro                                      | Descrizione                                                                                                                                                              | Valore |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_Archivio CAPICOM aperto in \_ \_ sola lettura \_**        | Aprire l'archivio in modalità di sola lettura.<br/>                                                                                                                             | 0     |
| **\_Archivio CAPICOM \_ aperto lettura/ \_ \_ scrittura**       | Aprire l'archivio in modalità di lettura/scrittura.<br/>                                                                                                                            | 1     |
| **\_ \_ \_ massimo \_ consentito per l'archivio CAPICOM**  | Aprire l'archivio in modalità di lettura/scrittura se l'utente dispone di autorizzazioni di lettura/scrittura. Se l'utente non dispone di autorizzazioni di lettura/scrittura, aprire l'archivio in modalità di sola lettura.<br/> | 2     |
| **\_Archivio CAPICOM \_ aperto \_ \_ solo esistente**    | Apri solo archivi esistenti; non creare un nuovo archivio. Introdotta da capicol 2,0.<br/>                                                                              | 128   |
| **\_ \_ Archivio CAPICOM aperto \_ include \_ archiviato** | Includere i certificati archiviati quando si usa l'archivio. Introdotta da capicol 2,0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Commenti

Quando si usa l'enumerazione dell'archivio capicot \_ \_ \_ , è possibile usare solo una delle impostazioni seguenti.

-   \_Archivio CAPICOM aperto in \_ \_ sola lettura \_
-   \_Archivio CAPICOM \_ aperto lettura/ \_ \_ scrittura
-   \_ \_ \_ massimo \_ consentito per l'archivio CAPICOM

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> </dl>

 

 




