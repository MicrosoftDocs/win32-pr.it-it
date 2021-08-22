---
description: I consumer di traccia eventi possono elaborare eventi da uno o più provider.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Utilizzo di eventi (Traccia eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42761bed132c5416a99888e067a1192571a527f39506e8964d5ea0209135b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269361"
---
# <a name="consuming-events-event-tracing"></a>Utilizzo di eventi (Traccia eventi)

I consumer di traccia eventi possono elaborare eventi da uno o più provider. I consumer possono elaborare eventi da un file di log o in tempo reale. È possibile utilizzare gli eventi in tempo reale solo se il controller specifica la modalità di registrazione in tempo reale per la sessione. Per motivi di prestazioni, l'elaborazione in tempo reale non è consigliata prima di Windows Vista.

Per specificare la sessione di traccia da cui si desidera elaborare gli eventi, utilizzare la [**struttura EVENT \_ TRACE \_ LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) . È necessario inizializzare una copia di questa struttura per ogni file di log o sessione in tempo reale che si desidera elaborare.

Per utilizzare gli eventi da un file di log, impostare il **membro LogFileName** sul nome del file di log. Per utilizzare gli eventi della sessione in tempo reale, impostare il **membro LoggerName** sul nome della sessione. Questa struttura viene usata anche per specificare il callback [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) e il callback [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) o [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) usato per elaborare gli eventi.

-   [**EventRecordCallback:**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)riceve ed elabora tutti gli eventi (incluso l'evento di intestazione) da uno o più file di log e da una sessione in tempo reale. Questo callback viene implementato se si usano le funzioni helper dati di traccia per analizzare i dati dell'evento o se si desidera recuperare i metadati relativi all'evento.
-   [*EventCallback:*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)riceve ed elabora tutti gli eventi (incluso l'evento di intestazione) da uno o più file di log e da una sessione in tempo reale.
-   [*BufferCallback:*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)riceve ed elabora le informazioni di riepilogo sul buffer corrente, ad esempio gli eventi persi. ETW chiama il callback dopo il recapito di tutti gli eventi nel buffer al consumer. Il consumer può anche usare questo callback per annullare l'elaborazione degli eventi. Tuttavia, se si utilizzano eventi in tempo reale, ETW recapita gli eventi fino a quando il controller non arresta la sessione.

Dopo aver definito una o più sessioni di traccia, chiamare la [**funzione OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) per ogni sessione di traccia che si desidera elaborare. È possibile elaborare gli eventi da uno o più file di log, ma da una sola sessione in tempo reale. Si passa quindi l'elenco degli handle di sessione di traccia **restituiti da OpenTrace** alla [**funzione ProcessTrace.**](/windows/win32/api/evntrace/nf-evntrace-processtrace) La **funzione ProcessTrace** combina gli eventi, li ordina in ordine cronologico e quindi li recapita ai callback uno alla volta. Gli eventi possono essere filtrati in modo da includere solo quelli che rientrano in un intervallo di tempo specifico usando i *parametri StartTime* *ed EndTime.* La **funzione ProcessTrace** blocca il thread fino a quando il consumer non elabora tutti gli eventi nelle sessioni di traccia, [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) restituisce **FALSE** o non si [**chiama CloseTrace.**](/windows/win32/api/evntrace/nf-evntrace-closetrace)

**Prima di Windows Vista:** È possibile chiamare [**CloseTrace solo**](/windows/win32/api/evntrace/nf-evntrace-closetrace) dopo la [**fine di ProcessTrace.**](/windows/win32/api/evntrace/nf-evntrace-processtrace)

Per un esempio che illustra come utilizzare gli eventi pubblicati usando un file manifesto, MOF o TMF, vedere Recupero dei dati degli eventi [tramite TDH.](retrieving-event-data-using-tdh.md) Si noti che a partire Windows Vista, è consigliabile usare le funzioni dell'helper dati di traccia (TDH) per utilizzare gli eventi.

Per un esempio che illustra come utilizzare gli eventi pubblicati tramite MOF, vedere Recupero dei dati degli eventi [tramite MOF.](retrieving-event-data-using-mof.md)

 

 
