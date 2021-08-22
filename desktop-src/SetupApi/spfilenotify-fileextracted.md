---
description: La notifica SPFILENOTIFY FILEEXTRACTED viene inviata a una routine di callback da SetupIterateCabinet per indicare che un file è stato estratto dal file cab o che un'estrazione non è riuscita ed è stata annullata \_ l'elaborazione dell'archivio.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: SPFILENOTIFY_FILEEXTRACTED messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56b5028dec11cf2317be080fb82b79bf155be007c66abcbee33492aa229d6317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665111"
---
# <a name="spfilenotify_fileextracted-message"></a>MESSAGGIO SPFILENOTIFY \_ FILEEXTRACTED

La notifica **SPFILENOTIFY \_ FILEEXTRACTED** viene inviata a una routine di callback da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per indicare che un file è stato estratto dal file cab o che un'estrazione non è riuscita e che l'elaborazione dell'archivio è stata annullata.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a [**una struttura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sul percorso per il file estratto. Il **membro SourceFile** della struttura **FILEPATHS** contiene il percorso di origine completo del file cab. Il **membro TargetFile** fornisce il percorso di destinazione completo del file da installare nel sistema.

</dd> <dt>

*Param2* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback cab deve restituire uno dei valori seguenti.



| Codice restituito                                                                               | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NESSUN \_ ERRORE**</dt> </dl>  | Non si è verificato alcun errore. Continuare a elaborare l'archivio.<br/>                                                                                                                                |
| <dl> <dt>**ERRORE \_ XXX**</dt> </dl> | Si è verificato un errore del tipo specificato. [**SetupIterateCabinet restituirà**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) zero. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore specificato.<br/> |



 

> [!Note]  
> Non è disponibile alcuna routine di callback dell'archivio predefinita fornita con l'API di installazione. L'applicazione di installazione deve fornire una routine di callback per gestire le notifiche inviate dalla [**funzione SetupIterateCabinet.**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

