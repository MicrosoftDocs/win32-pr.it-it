---
description: I provider classici usano la funzione TraceEventInstance per tracciare gli eventi che fanno parte di una singola transazione. È anche possibile usare questa funzione per tracciare gli eventi padre/figlio.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Scrittura di eventi correlati in un provider classico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41443c0a05bd94e25ae4ca6a4549671c6aa0682b848660ca31683bb4bf8b75b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813813"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Scrittura di eventi correlati in un provider classico

[I](about-event-tracing.md) provider classici usano [**la funzione TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) per tracciare gli eventi che fanno parte di una singola transazione. È anche possibile usare questa funzione per tracciare gli eventi padre/figlio.

Prima di chiamare [**la funzione TraceEventInstance,**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) è necessario chiamare la [**funzione CreateTraceInstanceId**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) per ottenere un identificatore di transazione. Questa funzione genera un identificatore di transazione univoco ed esegue il mapping a un handle GUID di classe registrato. Gli handle per i GUID di classe registrati sono disponibili nei membri **RegHandle** delle strutture [**TRACE GUID \_ \_ REGISTRATION,**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) dopo la chiamata [**alla funzione RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) L'identificatore della transazione viene inserito nel **membro InstanceId** di una struttura [**EVENT INSTANCE \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) passata alla **funzione CreateTraceInstanceId.**

La struttura [**EVENT \_ INSTANCE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) passata alla funzione [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) è simile alla struttura [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (vedere Eventi di traccia [),](tracing-events.md)ad eccezione del fatto che contiene informazioni aggiuntive relative alle istanze e non contiene un **membro GUID.**

Le istanze di evento possono essere usate per stabilire una relazione gerarchica tra gli eventi. La [**funzione TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) accetta informazioni specifiche dell'istanza da due istanze di evento. Il *parametro pInstInfo* punta alla struttura [**EVENT INSTANCE \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) dell'istanza dell'evento e il parametro *pParentInstInfo* punta alla struttura **EVENT INSTANCE \_ \_ INFO** di un'istanza dell'evento padre. La definizione di un'istanza di evento "padre" è definita dall'applicazione. L'elemento padre può essere qualsiasi istanza già generata.

 

 
