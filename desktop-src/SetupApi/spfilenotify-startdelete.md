---
description: La notifica SPFILENOTIFY STARTDELETE viene inviata alla funzione \_ di callback quando la coda avvia un'operazione di eliminazione di file.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: SPFILENOTIFY_STARTDELETE messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e17edd2bdbf58be72d4c7b8d6841663787c4fb0074e5eefe322c51dab0f9a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964297"
---
# <a name="spfilenotify_startdelete-message"></a>MESSAGGIO SPFILENOTIFY \_ STARTDELETE

La **notifica SPFILENOTIFY \_ STARTDELETE** viene inviata alla funzione di callback quando la coda avvia un'operazione di eliminazione di file.


```C++
SPFILENOTIFY_STARTDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una [**struttura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Ha sempre il valore FILEOP \_ DELETE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**INTERRUZIONE \_ FILEOP**</dt> </dl> | Interrompere il commit della coda. La routine di callback deve chiamare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per indicare il motivo dell'interruzione. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **FALSE** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore impostato dalla routine di callback durante la chiamata a **SetLastError.**<br/> |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Eseguire l'operazione di copia del file.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | Ignorare l'operazione di copia corrente.<br/>                                                                                                                                                                                                                                                                                                                                  |



 

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

 

