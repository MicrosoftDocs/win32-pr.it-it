---
description: La notifica SPFILENOTIFY \_ ENDDELETE viene restituita alla routine di callback quando una coda completa un'operazione di eliminazione. Questa notifica viene inviata anche se l'utente annulla o si verifica un errore.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: SPFILENOTIFY_ENDDELETE messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638bf333c034ececd5a22536805b2adab970df9f15e70d9f4a9f161229937aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964604"
---
# <a name="spfilenotify_enddelete-message"></a>MESSAGGIO SPFILENOTIFY \_ ENDDELETE

La **notifica SPFILENOTIFY \_ ENDDELETE** viene restituita alla routine di callback quando una coda completa un'operazione di eliminazione. Questa notifica viene inviata anche se l'utente annulla o si verifica un errore.


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una [**struttura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) Il **membro Win32Error** della struttura **FILEPATHS** indica il risultato di un'operazione di copia.

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

 

 




