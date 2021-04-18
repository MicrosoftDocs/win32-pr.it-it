---
description: La \_ notifica SPFILENOTIFY STARTSUBQUEUE viene inviata alla funzione di callback quando la coda inizia a elaborare le operazioni nella coda secondaria Delete, Rename o Copy.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Messaggio SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318210"
---
# <a name="spfilenotify_startsubqueue-message"></a>\_Messaggio SPFILENOTIFY STARTSUBQUEUE

La notifica **SPFILENOTIFY \_ STARTSUBQUEUE** viene inviata alla funzione di callback quando la coda inizia a elaborare le operazioni nella coda secondaria Delete, Rename o Copy.


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Coda secondaria avviata. Questo parametro può essere uno dei valori FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.

</dd> <dt>

*Param2* 
</dt> <dd>

Numero di operazioni di copia, ridenominazione o eliminazione di file nella coda secondaria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, la routine di callback deve chiamare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specificando l'errore e quindi restituire zero. La funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituirà **false** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore impostato dalla routine di callback.

Se non si verificano errori, la routine di callback deve restituire un valore diverso da zero.

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

 

