---
description: La \_ notifica FILEestrata SPFILENOTIFY viene inviata a una routine di callback da SetupIterateCabinet per indicare che un file è stato estratto dall'armadio o che un'estrazione non è riuscita e l'elaborazione del cabinet è stata annullata.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Messaggio SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318214"
---
# <a name="spfilenotify_fileextracted-message"></a>SPFILENOTIFY \_ messaggio FILEestraente

La **notifica \_ fileestrata SPFILENOTIFY** viene inviata a una routine di callback da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per indicare che un file è stato estratto dall'armadio o che un'estrazione non è riuscita e l'elaborazione del cabinet è stata annullata.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sul percorso per il file estratto. Il membro **SourceFile** della struttura **filePaths** contiene il percorso di origine completo del file CAB. Il membro **TargetFile** fornisce il percorso di destinazione completo del file da installare nel sistema.

</dd> <dt>

*Param2* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback del cabinet deve restituire uno dei valori seguenti.



| Codice restituito                                                                               | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Nessun \_ errore**</dt> </dl>  | Non è stato rilevato alcun errore, continuare l'elaborazione del file CAB.<br/>                                                                                                                                |
| <dl> <dt>**ERRORE \_ xxx**</dt> </dl> | Si è verificato un errore del tipo specificato. [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) restituirà zero. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore specificato.<br/> |



 

> [!Note]  
> Non esiste alcuna routine di callback predefinita del cabinet fornita con l'API di installazione. L'applicazione di installazione deve fornire una routine di callback per gestire le notifiche inviate dalla funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

