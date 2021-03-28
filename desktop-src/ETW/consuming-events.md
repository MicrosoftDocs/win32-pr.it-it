---
description: Gli utenti di traccia eventi possono elaborare gli eventi da uno o più provider.
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: Utilizzo di eventi (traccia eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad8234cc66d07b5a52c10ab39c7d7b3c8aa029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980855"
---
# <a name="consuming-events-event-tracing"></a>Utilizzo di eventi (traccia eventi)

Gli utenti di traccia eventi possono elaborare gli eventi da uno o più provider. I consumer possono elaborare gli eventi da un file di log o in tempo reale. È possibile utilizzare gli eventi in tempo reale solo se il controller specifica la modalità di registrazione in tempo reale per la sessione. Per motivi di prestazioni, l'elaborazione in tempo reale non è consigliata prima di Windows Vista.

Per specificare la sessione di traccia da cui si desidera elaborare gli eventi, è possibile utilizzare la struttura di [**\_ \_ log di traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) . È necessario inizializzare una copia di questa struttura per ogni file di log o sessione in tempo reale che si desidera elaborare.

Per utilizzare gli eventi da un file di log, impostare il membro **LogFileName** sul nome del file di log. Per utilizzare gli eventi della sessione in tempo reale, impostare il membro **loggername** sul nome della sessione. Questa struttura viene utilizzata anche per specificare il callback [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) e il callback [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) o [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) utilizzato per elaborare gli eventi.

-   [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback): riceve ed elabora tutti gli eventi, incluso l'evento di intestazione, da uno o più file di log e una sessione in tempo reale. Questo callback viene implementato se si utilizzano le funzioni di supporto dei dati di traccia per analizzare i dati dell'evento o si desidera recuperare i metadati relativi all'evento.
-   [*EventCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback): riceve ed elabora tutti gli eventi, incluso l'evento di intestazione, da uno o più file di log e una sessione in tempo reale.
-   [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka): riceve ed elabora le informazioni di riepilogo sul buffer corrente, ad esempio gli eventi persi. ETW chiama il callback dopo aver recapito tutti gli eventi nel buffer al consumer. Il consumer può inoltre utilizzare questo callback per annullare l'elaborazione degli eventi; Tuttavia, se si utilizzano eventi in tempo reale, ETW recapita gli eventi finché il controller non arresta la sessione.

Dopo aver definito una o più sessioni di traccia, chiamare la funzione [**OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) per ogni sessione di traccia che si desidera elaborare. è possibile elaborare gli eventi da uno o più file di log, ma solo da una sessione in tempo reale. Viene quindi passato l'elenco degli handle della sessione di traccia restituiti da **OpenTrace** alla funzione [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) . La funzione **ProcessTrace** combina gli eventi, li ordina in ordine cronologico e li recapita ai callback uno alla volta. Gli eventi possono essere filtrati in modo da includere solo quelli che rientrano in un intervallo di tempo specifico usando i parametri *StartTime* e *EndTime* . La funzione **ProcessTrace** blocca il thread fino a quando il consumer non elabora tutti gli eventi nelle sessioni di traccia, il [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) restituisce **false** oppure si chiama [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace).

**Prima di Windows Vista:** È possibile chiamare [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) solo dopo la restituzione di [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) .

Per un esempio in cui viene illustrato come utilizzare gli eventi pubblicati utilizzando un file manifesto, MOF o MDF, vedere [recupero di dati di evento tramite TDH](retrieving-event-data-using-tdh.md). Si noti che a partire da Windows Vista, è necessario utilizzare le funzioni helper dei dati di traccia (TDH) per utilizzare gli eventi.

Per un esempio in cui viene illustrato come utilizzare gli eventi pubblicati utilizzando MOF, vedere [recupero di dati di evento tramite MOF](retrieving-event-data-using-mof.md).

 

 
