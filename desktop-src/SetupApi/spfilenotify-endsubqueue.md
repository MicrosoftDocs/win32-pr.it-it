---
description: La notifica SPFILENOTIFY ENDSUBQUEUE viene inviata alla funzione di callback quando la coda completa tutte le operazioni nella coda secondaria di \_ eliminazione, ridenominazione o copia.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: SPFILENOTIFY_ENDSUBQUEUE messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72645aafbe94e3f90d11f8ccf65ed8c6006301db811bccd80936cadbf0478dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964550"
---
# <a name="spfilenotify_endsubqueue-message"></a>MESSAGGIO SPFILENOTIFY \_ ENDSUBQUEUE

La **notifica SPFILENOTIFY \_ ENDSUBQUEUE** viene inviata alla funzione di callback quando la coda completa tutte le operazioni nella coda secondaria di eliminazione, ridenominazione o copia.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Coda secondaria completata. Questo parametro può essere uno dei valori seguenti: FILEOP \_ DELETE, FILEOP \_ RENAME o FILEOP \_ COPY.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



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

 

 




