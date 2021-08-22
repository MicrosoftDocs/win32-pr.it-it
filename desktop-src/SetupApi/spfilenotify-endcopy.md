---
description: La notifica SPFILENOTIFY \_ ENDCOPY viene passata alla funzione di callback quando la coda completa un'operazione di copia. Questa notifica viene inviata anche se l'utente annulla o si verifica un errore.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: SPFILENOTIFY_ENDCOPY messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87b4a53e1dc88f8cdb7d2ec790cab82b66d8698c6f45abf97e2b5ac5b8511ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665131"
---
# <a name="spfilenotify_endcopy-message"></a>Messaggio SPFILENOTIFY \_ ENDCOPY

La **notifica SPFILENOTIFY \_ ENDCOPY** viene passata alla funzione di callback quando la coda completa un'operazione di copia. Questa notifica viene inviata anche se l'utente annulla o si verifica un errore.


```C++
SPFILENOTIFY_ENDCOPY
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

Il codice restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
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

 

 




