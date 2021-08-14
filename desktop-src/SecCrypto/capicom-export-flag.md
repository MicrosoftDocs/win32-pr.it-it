---
description: Il tipo di enumerazione CAPICOM EXPORT FLAG definisce se eventuali errori di esportazione della chiave \_ \_ privata vengono ignorati.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: CAPICOM_EXPORT_FLAG enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d6be9953640eeb2eb1d6c7fad812f5efe2d2da2f6888a01b4450c638ab68bfca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772466"
---
# <a name="capicom_export_flag-enumeration"></a>Enumerazione CAPICOM \_ EXPORT \_ FLAG

Il **tipo di enumerazione \_ CAPICOM EXPORT \_ FLAG** definisce se eventuali errori di esportazione della chiave privata vengono ignorati.

## <a name="members"></a>Membri



| Membro                                                            | Descrizione                                               | Valore |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **IMPOSTAZIONE PREDEFINITA \_ DELL'ESPORTAZIONE \_ CAPICOM**                                      | Eventuali errori di esportazione della chiave privata non vengono ignorati.<br/> | 0     |
| **ERRORE DI ESPORTAZIONE \_ CAPICOM \_ IGNORA CHIAVE PRIVATA NON \_ \_ \_ \_ \_ ESPORTABILE** | Eventuali errori di esportazione della chiave privata vengono ignorati.<br/>     | 1     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione \_ CAPICOM EXPORT \_ FLAG viene usato dal metodo seguente:

-   [**Certificates.Save**](certificates-save.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




