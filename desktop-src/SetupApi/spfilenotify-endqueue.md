---
description: La \_ notifica SPFILENOTIFY ENDQUEUE viene inviata alla routine di callback quando tutte le operazioni in coda sono state completate.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Messaggio SPFILENOTIFY_ENDQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968499"
---
# <a name="spfilenotify_endqueue-message"></a>\_Messaggio SPFILENOTIFY ENDQUEUE

La notifica **SPFILENOTIFY \_ ENDQUEUE** viene inviata alla routine di callback quando tutte le operazioni in coda sono state completate.


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

**True** se la coda è stata elaborata correttamente; in caso contrario, **false** .

</dd> <dt>

*Param2* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Overview](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




