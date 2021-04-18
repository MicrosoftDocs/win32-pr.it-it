---
description: La \_ notifica SPFILENOTIFY NEEDMEDIA viene inviata alla routine di callback quando è necessario un nuovo file multimediale o un nuovo file CAB.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Messaggio SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320637"
---
# <a name="spfilenotify_needmedia-message"></a>\_Messaggio SPFILENOTIFY NEEDMEDIA

La notifica **SPFILENOTIFY \_ NEEDMEDIA** viene inviata alla routine di callback quando è necessario un nuovo file multimediale o un nuovo file CAB.


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura del [**\_ supporto di origine**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Puntatore a una matrice di caratteri per archiviare le nuove informazioni sul percorso fornite dall'utente. La dimensione del buffer è una matrice **TCHAR** di \_ elementi di percorso max. Le informazioni sul percorso restituite dall'applicazione di installazione non devono superare questa dimensione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei seguenti elementi.



| Codice restituito                                                                                    | Descrizione                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_NEWPATH FILEOP**</dt> </dl> | Il supporto è presente e il file richiesto è disponibile nel percorso specificato nel buffer a cui punta *param2*.<br/>                                                                                         |
| <dl> <dt>**\_Ignora FILEOP**</dt> </dl>    | Ignora il file richiesto<br/>                                                                                                                                                                                      |
| <dl> <dt>**\_interruzione FILEOP**</dt> </dl>   | Interrompi elaborazione coda. La funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **false**. GetLastError restituisce informazioni estese sull'errore, ad esempio errore \_ annullato se l'utente è stato annullato.<br/> |
| <dl> <dt>**FILEOP-DOIT**</dt> </dl>     | Il supporto è disponibile.<br/>                                                                                                                                                                                      |



 

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
</dt> <dt>

[**supporto di origine \_**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




