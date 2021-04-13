---
description: "\\_Se si verifica un errore durante un'operazione di ridenominazione dei file, viene inviata la notifica SPFILENOTIFY RENAMEERROR alla routine di callback."
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Messaggio SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347246"
---
# <a name="spfilenotify_renameerror-message"></a>\_Messaggio SPFILENOTIFY RENAMEERROR

Se si verifica un errore durante un'operazione di ridenominazione dei file, viene inviata la notifica **SPFILENOTIFY \_ RENAMEERROR** alla routine di callback.


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . Il membro **Win32Error** della struttura **filePaths** specifica l'errore che si è verificato durante l'operazione di ridenominazione.

</dd> <dt>

*Param2* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei seguenti elementi.



| Codice restituito                                                                                  | Descrizione                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ nuovo tentativo**</dt> </dl> | L'utente ha scelto di ritentare l'operazione di ridenominazione.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**\_Ignora FILEOP**</dt> </dl>  | L'utente ha scelto di ignorare l'operazione di ridenominazione dei file.<br/>                                                                                                                                                                                                      |
| <dl> <dt>**\_interruzione FILEOP**</dt> </dl> | Arrestare il commit della coda. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **false**. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio errore \_ annullato (se l'utente è stato annullato) o errore \_ \_ memoria insufficiente \_ .<br/> |



 

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

 

