---
description: I provider classici usano la funzione TraceEventInstance per tracciare gli eventi che fanno parte di una singola transazione. È anche possibile usare questa funzione per tracciare gli eventi padre/figlio.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Scrittura di eventi correlati in un provider classico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771b08a66625d5cd6e723fbc2e12eed87bd1d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350326"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Scrittura di eventi correlati in un provider classico

I provider [classici](about-event-tracing.md) usano la funzione [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) per tracciare gli eventi che fanno parte di una singola transazione. È anche possibile usare questa funzione per tracciare gli eventi padre/figlio.

Prima di chiamare la funzione [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) , è necessario chiamare prima la funzione [**CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) per ottenere un identificatore di transazione. Questa funzione genera un identificatore univoco della transazione e ne esegue il mapping a un handle GUID della classe registrato. Gli handle per i GUID della classe registrati sono disponibili nei membri **RegHandle** delle strutture di [**\_ \_ registrazione del GUID di traccia**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) , dopo la chiamata della funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . L'identificatore della transazione viene inserito nel membro **InstanceID** di una struttura di [**\_ \_ informazioni sull'istanza dell'evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) passata alla funzione **CreateTraceInstanceId** .

La struttura dell' [**\_ \_ intestazione dell'istanza di evento**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) passata alla funzione [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) è simile alla struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (vedere [eventi di traccia](tracing-events.md)), ad eccezione del fatto che contiene informazioni aggiuntive relative alle istanze di e non contiene un membro **GUID** .

Le istanze di evento possono essere utilizzate per stabilire una relazione gerarchica tra gli eventi. La funzione [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) accetta informazioni specifiche dell'istanza da due istanze dell'evento. Il parametro *pInstInfo* punta alla struttura [**di \_ \_ informazioni sull'istanza**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) dell'evento e il parametro *pParentInstInfo* punta alla struttura di **\_ \_ informazioni sull'istanza dell'evento** di un'istanza dell'evento padre. La definizione di un'istanza di evento "padre" è definita dall'applicazione; l'elemento padre può essere qualsiasi istanza che è già stata generata.

 

 
