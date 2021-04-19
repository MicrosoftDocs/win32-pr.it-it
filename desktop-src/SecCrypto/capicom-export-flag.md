---
description: Il \_ tipo di enumerazione del flag di esportazione CAPICOM \_ definisce se eventuali errori di esportazione della chiave privata vengono ignorati.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Enumerazione CAPICOM_EXPORT_FLAG (CAPICOM. h)
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
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327647"
---
# <a name="capicom_export_flag-enumeration"></a>\_Enumerazione del flag di esportazione CAPICOM \_

Il tipo di enumerazione del **\_ \_ flag di esportazione CAPICOM** definisce se eventuali errori di esportazione della chiave privata vengono ignorati.

## <a name="members"></a>Membri



| Membro                                                            | Descrizione                                               | Valore |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **impostazione predefinita per l'esportazione di CAPICOM \_ \_**                                      | Eventuali errori di esportazione della chiave privata non vengono ignorati.<br/> | 0     |
| **errore di esportazione di CAPICOM \_ \_ Ignora \_ \_ chiave privata \_ non \_ esportabile \_** | Eventuali errori di esportazione della chiave privata vengono ignorati.<br/>     | 1     |



## <a name="remarks"></a>Commenti

Il \_ \_ tipo di enumerazione del flag di esportazione CAPICOM viene utilizzato dal metodo seguente:

-   [**Certificati. Salva**](certificates-save.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




