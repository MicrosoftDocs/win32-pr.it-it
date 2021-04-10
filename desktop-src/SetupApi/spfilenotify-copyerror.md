---
description: "\\_Quando si verifica un errore durante un'operazione di copia file, viene inviata la notifica SPFILENOTIFY COPYERROR alla routine di callback."
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Messaggio SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882358"
---
# <a name="spfilenotify_copyerror-message"></a>\_Messaggio SPFILENOTIFY COPYERROR

Quando si verifica un errore durante un'operazione di copia file, viene inviata la notifica **SPFILENOTIFY \_ COPYERROR** alla routine di callback.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Puntatore a un buffer, con dimensioni MASSIMe dei \_ caratteri di percorso, in cui sono archiviate le nuove informazioni sul percorso specificate dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_interruzione FILEOP**</dt> </dl>   | L'elaborazione della coda deve essere annullata. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio errore \_ annullato (se l'utente è stato annullato) o errore di \_ \_ memoria insufficiente \_ .<br/> |
| <dl> <dt>**\_NEWPATH FILEOP**</dt> </dl> | Ripetere l'operazione di copia utilizzando il percorso della funzione di callback posizionata nel buffer a cui punta il parametro *param2* . La routine di callback deve garantire che il percorso non superi le dimensioni del buffer di una matrice TCHAR di \_ elementi di percorso max.<br/>                |
| <dl> <dt>**FILEOP \_ nuovo tentativo**</dt> </dl>   | L'utente sta tentando di eseguire di nuovo l'operazione di copia.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**\_Ignora FILEOP**</dt> </dl>    | L'utente sta ignorando l'operazione di copia del file.<br/>                                                                                                                                                                                                                      |



 

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

 

