---
title: RPC_STATUS (rpcdce. h)
description: Lo stato RPC del tipo \_ di dati rappresenta un tipo di codice di stato specifico della piattaforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048330"
---
# <a name="rpc_status"></a>\_stato RPC

Lo **\_ stato RPC** del tipo di dati rappresenta un tipo di codice di stato specifico della piattaforma.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Commenti

Il tipo di **\_ stato RPC** viene restituito dalla maggior parte delle funzioni RPC ed è parte della definizione del tipo di funzione [**\_ \_ INQ \_ FN dell'oggetto RPC**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h (include RPC. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_oggetto RPC \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





