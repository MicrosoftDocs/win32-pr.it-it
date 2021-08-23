---
description: La notifica SPFILENOTIFY ENDRENAME viene inviata alla routine di callback quando \_ la coda completa un'operazione di ridenominazione. Questa notifica viene inviata anche se l'utente annulla o si verifica un errore.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: SPFILENOTIFY_ENDRENAME messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f34ad30cc103e8a13277d3383bad8c2e46409eaabe6f957ace27aebc9759990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683121"
---
# <a name="spfilenotify_endrename-message"></a>SPFILENOTIFY \_ ENDRENAME message

La **notifica SPFILENOTIFY \_ ENDRENAME viene** inviata alla routine di callback quando la coda completa un'operazione di ridenominazione. Questa notifica viene inviata anche se l'utente annulla o si verifica un errore.


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una [**struttura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) Il **membro Win32Error** della struttura **FILEPATHS** indica il risultato dell'operazione di copia.

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

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




