---
description: Poiché l'API di installazione non fornisce una routine di callback del cabinet predefinita, è necessario specificare una routine. La routine di callback necessaria per la funzione SetupIterateCabinet deve avere lo stesso formato di quelle a cui punta filecallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Creazione di una routine di callback del cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231840"
---
# <a name="creating-a-cabinet-callback-routine"></a>Creazione di una routine di callback del cabinet

Poiché l'API di installazione non fornisce una routine di callback del cabinet predefinita, è necessario specificare una routine. La routine di callback necessaria per la funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) deve avere lo stesso formato di quelle a cui punta [filecallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).

Di seguito è riportata la sintassi utilizzata da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per inviare una notifica alla routine di callback.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Il parametro *context* è un puntatore void a una variabile di contesto o a una struttura che può essere utilizzata dalla routine di callback per archiviare le informazioni che devono essere mantenute tra le chiamate successive alla routine di callback.

Questa implementazione del contesto è specificata dalla routine di callback e non viene mai fatto riferimento o modificata da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

Il parametro *Notification* è un Unsigned Integer e sarà uno dei valori seguenti.



| Notifica                                                        | Descrizione                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**SPFILENOTIFY \_ FILEextracted**](spfilenotify-fileextracted.md)   | Il file è stato estratto dal file CAB.      |
| [**\_FILEINCABINET SPFILENOTIFY**](spfilenotify-fileincabinet.md)   | Viene rilevato un file nell'archivio.              |
| [**\_NEEDNEWCABINET SPFILENOTIFY**](spfilenotify-neednewcabinet.md) | Il file corrente viene continuato nel file CAB successivo. |



 

I due parametri finali, *param1* e *param2*, sono anche interi senza segno e contengono informazioni aggiuntive relative alla notifica. Per ulteriori informazioni sulle notifiche inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), vedere la pagina relativa alle [notifiche dei file CAB](cabinet-file-notifications.md).

Una \_ routine di callback di notifica file SP \_ \_ restituisce un Unsigned Integer. La routine di callback del cabinet deve restituire uno dei valori seguenti a seconda della notifica.

Per la \_ notifica SPFILENOTIFY FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) prevede che uno dei valori seguenti venga restituito dalla routine di callback.



| Valore         | Significato                   |
|---------------|---------------------------|
| \_interruzione FILEOP | Interrompi elaborazione del cabinet. |
| \_doit FILEOP  | Estrarre il file corrente. |
| \_Ignora FILEOP  | Ignora il file corrente.    |



 

Per \_ \_ le notifiche fileestrate SPFILENOTIFY NEEDNEWCABINET e SPFILENOTIFY, **SetupIterateCabinet** prevede che venga restituito uno dei valori seguenti dalla routine di callback.



| Valore      | Significato                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessun \_ errore  | Non è stato rilevato alcun errore, continuare l'elaborazione del file CAB.                                                                                                                                                                        |
| ERRORE \_ xxx | Si è verificato un errore del tipo specificato. La funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) restituirà **false** e il codice di errore specificato verrà restituito da una chiamata a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). |



 

Se la routine di callback restituisce FILEOP \_ doit, la routine deve fornire anche un percorso di destinazione completo. Per altre informazioni, vedere [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).

 

 
