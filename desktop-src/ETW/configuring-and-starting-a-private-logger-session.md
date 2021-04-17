---
description: Una sessione di traccia eventi privata è una sessione di traccia eventi in modalità utente eseguita nello stesso processo dei provider di traccia eventi&\# 8212; la sessione privata e i provider abilitati devono essere tutti nello stesso processo.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurazione e avvio di una sessione di logger privata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485277"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Configurazione e avvio di una sessione di logger privata

Una sessione di traccia eventi privata è una sessione di traccia eventi in modalità utente eseguita nello stesso processo dei provider di traccia eventi, ovvero la sessione privata e i provider abilitati devono essere tutti nello stesso processo. Il vantaggio dell'utilizzo di una sessione privata è che la sessione privata non viene conteggiata rispetto al numero massimo di 64 sessioni di traccia eventi eseguite simultaneamente.

La configurazione e l'avvio di una sessione privata sono simili all'avvio di una normale sessione di traccia eventi. La differenza è che il membro **WNODE. Guid** della struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) deve contenere il **GUID** del provider e non la sessione e il provider deve avere già registrato il GUID. Si noti che se si imposta anche la \_ traccia eventi \_ privata \_ in \_ modalità di registrazione proc, è possibile usare un **GUID** diverso per la sessione e il provider. Per informazioni dettagliate sull'avvio di una normale sessione di traccia eventi, vedere [configurazione e avvio di una sessione](configuring-and-starting-an-event-tracing-session.md)di traccia eventi.

Si noti che non è possibile avviare, arrestare o scaricare una sessione di traccia privata da DllMain; è consigliabile eseguire questa operazione nelle routine di inizializzazione e finalizzazione della DLL.

Da Windows 8.1 a Windows 10, la versione 1607, il payload dell'evento, l'ambito e i filtri di percorso stack possono essere usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**enable \_ trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descrittore filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger. Per ulteriori informazioni sui filtri di payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **enable \_ trace \_ Parameters**, **Event \_ Filter \_ descrittor** e [**payload \_ Filter \_ predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .

A partire da Windows 10, versione 1703, gli utenti con privilegi limitati possono ora avviare una sessione di logger privata nei processi avviati. Il provider non deve più essere registrato prima di abilitare o avviare la sessione privata, vale a dire che il provider è "preabilitato" in modo analogo a come sono i provider di sessione non privati. È previsto un limite di 8 logger privati a livello di sistema per un singolo processo. Per migliorare le prestazioni negli scenari tra processi, è consigliabile usare il filtro per le API di sessione (incluse [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) quando si avvia un logger privato a livello di sistema. Si noti che gli stessi filtri devono essere passati a tutte le API di sessione. Per ulteriori informazioni sui filtri, vedere [**\_ proprietà della traccia eventi \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

Per informazioni dettagliate sull'avvio di una sessione del logger di kernel NT, vedere [configurazione e avvio della sessione del logger di kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione di logger globale, vedere [configurazione e avvio di una sessione di logger globale](configuring-and-starting-the-global-logger-session.md).

Per informazioni dettagliate sull'avvio di una sessione di autologger, vedere [configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md).

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

[**Abilita \_ parametri di traccia \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_proprietà della traccia eventi \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_Proprietà della traccia eventi \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**\_descrittore filtro eventi \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_predicato filtro payload \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
