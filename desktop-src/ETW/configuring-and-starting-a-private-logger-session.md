---
description: Una sessione di traccia eventi privata è una sessione di traccia eventi in modalità utente che viene eseguita nello stesso processo dei provider di traccia eventi&8212; la sessione privata e i provider abilitati devono essere tutti nello \# stesso processo.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurazione e avvio di una sessione privata del logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf15db05c03e5a412cf07ee6e020d2321380f2d48abba465669dc807729fe38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901501"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configurazione e avvio di una sessione privata del logger

Una sessione di traccia eventi privata è una sessione di traccia eventi in modalità utente che viene eseguita nello stesso processo dei relativi provider di traccia eventi, ovvero la sessione privata e i provider abilitati devono essere tutti nello stesso processo. Il vantaggio dell'uso di una sessione privata è che la sessione privata non viene conteggiato rispetto al numero massimo di 64 sessioni di traccia eventi in esecuzione contemporaneamente.

La configurazione e l'avvio di una sessione privata sono simili all'avvio di una normale sessione di traccia eventi. La differenza è che il membro **Wnode.Guid** della struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) deve contenere il **GUID** del provider, non la sessione, e il provider deve aver già registrato il GUID. Si noti che se si imposta anche la modalità di registrazione EVENT TRACE PRIVATE IN PROC, è possibile usare un GUID diverso per la sessione \_ \_ e il \_ \_ provider.  Per informazioni dettagliate sull'avvio di una normale sessione di traccia eventi, vedere [Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

Si noti che non è possibile avviare, arrestare o scaricare una sessione di traccia privata da DllMain. È consigliabile eseguire questa operazione nelle routine di inizializzazione e finalizzazione della DLL.

Da Windows 8.1 a Windows 10, la versione 1607, il payload dell'evento, l'ambito e i filtri di analisi dello stack possono essere usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger. Per altre informazioni sui filtri del payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** e [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

A partire Windows 10 versione 1703, gli utenti con privilegi minimi possono ora avviare una sessione del logger privato nei processi avviati. Il provider non deve più essere registrato prima di abilitare o avviare la sessione privata, vale a dire che il provider è pre-abilitato in modo simile a come sono i provider di sessione non privati. È previsto un limite di 8 logger privati a livello di sistema a un singolo processo. Per migliorare le prestazioni negli scenari tra processi, è consigliabile usare il filtro per le API di sessione (inclusi [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) [**QueryTrace,**](/windows/win32/api/evntrace/nf-evntrace-querytrace) [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e [**StopTrace)**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)quando si avvia un logger privato a livello di sistema. Si noti che gli stessi filtri devono essere passati a tutte le API di sessione. Per altre informazioni sui filtri, vedere [**EVENT \_ TRACE PROPERTIES \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

Per informazioni dettagliate sull'avvio di una sessione del logger del kernel NT, vedere Configurazione e [avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione del logger globale, vedere Configurazione e [avvio di una sessione del logger globale](configuring-and-starting-the-global-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione di AutoLogger, vedere [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**ABILITARE \_ I PARAMETRI DI \_ TRACCIA**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**PROPRIETÀ \_ DI TRACCIA \_ EVENTI**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**PROPRIETÀ \_ DI TRACCIA EVENTI \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**DESCRITTORE \_ DEL \_ FILTRO EVENTI**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PREDICATO \_ DEL \_ FILTRO PAYLOAD**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
