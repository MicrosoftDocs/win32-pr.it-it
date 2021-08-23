---
description: La notifica SPFILENOTIFY STARTRENAME viene inviata alla funzione di callback quando la coda \_ avvia un'operazione di ridenominazione di file.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: SPFILENOTIFY_STARTRENAME messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ec75c84841adf5cb8a187e8d8431f031af74b31f33af7a87e46225b1e9a3464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739421"
---
# <a name="spfilenotify_startrename-message"></a>SPFILENOTIFY \_ STARTRENAME message

La **notifica SPFILENOTIFY \_ STARTRENAME viene** inviata alla funzione di callback quando la coda avvia un'operazione di ridenominazione di file.


```C++
SPFILENOTIFY_STARTRENAME
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

Ha sempre il valore FILEOP \_ RENAME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**INTERRUZIONE \_ FILEOP**</dt> </dl> | Interrompere il commit della coda. La routine di callback deve [**chiamare SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per indicare il motivo della terminazione. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **FALSE** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore impostato dalla routine di callback durante la chiamata a **SetLastError.**<br/> |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Eseguire l'operazione di copia del file.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | Ignorare l'operazione di copia corrente.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

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

 

