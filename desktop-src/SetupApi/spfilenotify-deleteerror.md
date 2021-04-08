---
description: "\\_Se si verifica un errore durante un'operazione di eliminazione di file, la notifica SPFILENOTIFY DELETEERROR viene inviata alla routine di callback."
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Messaggio SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058272"
---
# <a name="spfilenotify_deleteerror-message"></a>\_Messaggio SPFILENOTIFY DELETEERROR

Se si verifica un errore durante un'operazione di eliminazione di file, la notifica **SPFILENOTIFY \_ DELETEERROR** viene inviata alla routine di callback.


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_interruzione FILEOP**</dt> </dl> | L'elaborazione della coda deve essere annullata. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio errore \_ annullato (se l'utente è stato annullato) o errore di \_ \_ memoria insufficiente \_ .<br/> |
| <dl> <dt>**FILEOP \_ nuovo tentativo**</dt> </dl> | L'utente sta tentando di eseguire di nuovo l'operazione di eliminazione.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**\_Ignora FILEOP**</dt> </dl>  | L'utente sta ignorando l'operazione di eliminazione del file.<br/>                                                                                                                                                                                                                    |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

