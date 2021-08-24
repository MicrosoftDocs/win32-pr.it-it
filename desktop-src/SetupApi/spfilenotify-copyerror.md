---
description: La notifica SPFILENOTIFY COPYERROR viene inviata alla routine di callback se si verifica \_ un errore durante un'operazione di copia di file.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: SPFILENOTIFY_COPYERROR messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80160af9d8053a90c1848d397da6bbb9bf41f2793756e1d5491fb0d6f5e39abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665151"
---
# <a name="spfilenotify_copyerror-message"></a>MESSAGGIO SPFILENOTIFY \_ COPYERROR

La **notifica SPFILENOTIFY \_ COPYERROR** viene inviata alla routine di callback se si verifica un errore durante un'operazione di copia di file.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una [**struttura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)

</dd> <dt>

*Param2* 
</dt> <dd>

Puntatore a un buffer, di dimensioni massime caratteri PATH, in cui \_ sono archiviate le nuove informazioni sul percorso specificate dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**INTERRUZIONE \_ FILEOP**</dt> </dl>   | L'elaborazione della coda deve essere annullata. [**SetupCommitFileQueue restituisce**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce informazioni estese sull'errore, ad esempio ERROR CANCELLED (se l'utente ha annullato) o \_ ERROR NOT ENOUGH \_ \_ \_ MEMORY.<br/> |
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | Ripetere l'operazione di copia usando il percorso della funzione di callback inserita nel buffer a cui punta *il parametro Param2.* La routine di callback deve garantire che il percorso non eserciti l'overflow delle dimensioni del buffer di una matrice TCHAR di elementi MAX \_ PATH.<br/>                |
| <dl> <dt>**NUOVO TENTATIVO DI \_ FILEOP**</dt> </dl>   | L'utente sta tentando di eseguire nuovamente l'operazione di copia.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | L'utente sta ignorando l'operazione di copia del file.<br/>                                                                                                                                                                                                                      |



 

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

 

