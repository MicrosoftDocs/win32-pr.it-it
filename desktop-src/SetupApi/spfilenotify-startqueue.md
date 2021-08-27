---
description: La notifica SPFILENOTIFY \_ STARTQUEUE viene inviata alla routine di callback all'avvio del processo di impegno della coda.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: SPFILENOTIFY_STARTQUEUE messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40d4fedde850d975edd697423339c686fe697911b9bef2fdc252baffda0158f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073211"
---
# <a name="spfilenotify_startqueue-message"></a>SPFILENOTIFY \_ STARTQUEUE message

La **notifica SPFILENOTIFY \_ STARTQUEUE** viene inviata alla routine di callback all'avvio del processo di impegno della coda.


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Handle per la finestra proprietaria delle finestre di dialogo generate dalla routine di callback.

</dd> <dt>

*Param2* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, la routine di callback deve chiamare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specificando l'errore e quindi restituire zero. La [**funzione SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituirà **FALSE** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore impostato dalla routine di callback.

Se non si verifica alcun errore, la routine di callback deve restituire un valore diverso da zero.

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

 

