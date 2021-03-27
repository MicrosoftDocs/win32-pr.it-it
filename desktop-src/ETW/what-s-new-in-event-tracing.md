---
description: In questa sezione vengono descritte le nuove funzionalità aggiunte a Event Tracing for Windows in ogni versione.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Novità della traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613433834e5a11f2886b6ee314fdb60114f66976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753031"
---
# <a name="whats-new-in-event-tracing"></a>Novità della traccia eventi

In questa sezione vengono descritte le nuove funzionalità aggiunte a Event Tracing for Windows in ogni versione.

## <a name="windows-10-version-1709"></a>Windows 10, versione 1709

ETW ora può tenere traccia dei file binari per tutti i provider abilitati per la sessione. Il rilevamento viene applicato in modo retroattivo per i provider che sono stati abilitati per la sessione prima della chiamata, nonché per tutti i provider futuri abilitati per la sessione. È anche possibile eseguire una query per il numero massimo di logger di sistema attualmente configurato consentito dal sistema operativo. Per ulteriori informazioni, vedere i valori **TraceProviderBinaryTracking** e **TraceMaxLoggersQuery** dell'enumerazione [**della \_ \_ classe Trace Info**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , oltre a [recuperare ulteriori dati di traccia eventi](retrieving-additional-event-tracing-data.md).

ETW ora può filtrare gli eventi in base al nome dell'evento. È anche possibile determinare gli eventi in cui vengono acquisiti gli stack. Per ulteriori informazioni, vedere il nome dell'evento del tipo di filtro eventi, il **tipo di \_ filtro eventi \_ \_ STACKWALK \_** e il tipo di **\_ filtro evento \_ \_ STACKWALK \_ level \_ kW** valori della struttura del [**\_ \_ descrittore di filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) , nonché il [**\_ \_ \_ nome dell'evento filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) associato e le strutture del [**\_ \_ \_ livello filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) . **\_ \_ \_ \_**

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) si basa su ETW e fornisce un modo semplificato per instrumentare il codice per gli sviluppatori nativi, .NET e WinRT. TraceLogging consente di includere dati strutturati con eventi, correlare gli eventi e non richiede un file XML del manifesto di strumentazione separato.

I [tratti del provider](provider-traits.md) sono stati aggiunti come metodo per il fissaggio di più dati a una registrazione del singolo provider. Possono essere usati per provider TraceLogging o basati su manifesto. Questo include attualmente il supporto per l'aggiunta di un nome di provider e/o di un gruppo di provider a una singola registrazione del provider. I gruppi di provider sono una nuova funzionalità che consente di controllare più provider ETW in modo aggregato dal gruppo a cui appartengono.

Lo stato di acquisizione periodico consente di inviare periodicamente le notifiche dello stato di acquisizione ai provider. Quando questa funzionalità è abilitata, le notifiche verranno inviate solo alle registrazioni del provider che sono state precedentemente abilitate per la sessione corrente. Ogni provider può definire la propria risposta, se presente, a una notifica. Per informazioni dettagliate sull'implementazione, vedere [**\_ \_ \_ \_ informazioni sullo stato di acquisizione periodica della traccia**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Le funzionalità seguenti sono state aggiunte alla traccia eventi in Windows 8.1 e Windows Server 2012 R2.

Funzioni che supportano l'utilizzo dei filtri per payload di eventi, ambito e percorso stack utilizzati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e le strutture [**enable \_ trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descrittore filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione logger. Per altre informazioni, vedere:

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Vedere inoltre la documentazione dettagliata per la funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e le strutture [**enable \_ trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descrittore filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) utilizzati da queste funzionalità.

Struttura che definisce un predicato del filtro del payload dell'evento che descrive come filtrare in base a un singolo campo di una sessione di traccia utilizzata dalla nuova funzione [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) e una nuova struttura utilizzata dai filtri ID evento e percorso stack. Per altre informazioni, vedere:

-   [**\_ \_ ID evento filtro \_ eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**\_predicato filtro payload \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funzioni che recuperano informazioni sugli eventi presenti nel manifesto del provider. Per altre informazioni, vedere:

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Struttura che definisce una matrice di eventi in un manifesto del provider utilizzato dalla nuova funzione [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) . Per altre informazioni, vedere:

-   [**\_informazioni evento \_ provider**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Le funzionalità seguenti sono state aggiunte alla traccia eventi in Windows 8 e Windows Server 2012.

Funzioni che eseguono operazioni su un oggetto di registrazione, forniscono analisi del payload dell'evento, forniscono l'esplorazione del provider di tracce, le impostazioni della sessione di traccia eventi di query e l'elaborazione di un file di traccia registrato. Per altre informazioni, vedere:

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Interfacce che forniscono informazioni al relogger nel processo di traccia e quando vengono registrati gli eventi, l'accesso ai dati per un evento specifico e l'accesso alle funzionalità del logger che consentono la manipolazione dei file di log di traccia eventi (ETL). Per altre informazioni, vedere:

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Enumerazioni aggiuntive utilizzate dalle nuove funzioni e interfacce. Per altre informazioni, vedere:

-   [**\_classe informazioni \_ evento**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**\_ \_ classe informazioni query di traccia \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

In questa versione sono state aggiunte le funzionalità seguenti:

-   Possibilità per i provider di definire i filtri nel manifesto. In Windows Vista, i controller potevano passare i dati del filtro al provider. Tuttavia, il layout dei dati del filtro non è stato definito nel manifesto, quindi il provider deve utilizzare altri mezzi per fornire la definizione del filtro ai controller. Con questa versione, i provider possono definire la definizione di filtro nel manifesto (vedere l'attributo **Filters** del tipo complesso [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md) ). I controller possono quindi utilizzare la funzione [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) per determinare la definizione del filtro. I provider che utilizzano i filtri devono utilizzare la funzione [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) per scrivere l'evento.
-   Possibilità di usare un singolo buffer per raccogliere gli eventi generati su più processori. L'utilizzo di un singolo buffer Elimina la visualizzazione degli eventi non in ordine nei computer con più processori. Per informazioni dettagliate, vedere la modalità di registrazione del [**\_ buffer di traccia eventi \_ No \_ per \_ processore \_**](logging-mode-constants.md) . Per impostazione predefinita, ETW usa i buffer per processore.
-   Possibilità di acquisire una traccia dello stack per gli eventi. Per abilitare la traccia dello stack per gli eventi del kernel, vedere la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . Per abilitare la traccia dello stack per gli eventi utente, vedere il flag di **\_ \_ \_ \_ traccia dello stack di proprietà dell'evento** per il membro **EnableProperty** di [**Abilita \_ \_ parametri di traccia**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   Possibilità di specificare la modalità di registrazione del **\_ buffer della traccia \_ \_** eventi o della modalità **\_ file di traccia eventi \_ \_ \_** con la modalità di registrazione in modalità **\_ \_ \_ logger \_ privato della traccia** eventi (vedere [costanti della modalità di registrazione](logging-mode-constants.md)).
-   Possibilità di abilitare un provider in modo sincrono. Per impostazione predefinita, i provider sono abilitati in modo asincrono. Per abilitare un provider in modo sincrono, impostare il parametro *timeout* di [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   Possibilità per il controller di richiedere che il provider registri il proprio stato. Per informazioni dettagliate, vedere il flag di stato di acquisizione del codice di controllo dell'evento per il parametro *ControlCode* di [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2). **\_ \_ \_ \_**
-   Possibilità per gli utenti di formattare i dati degli eventi tramite la funzione [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) .
-   Possibilità di decodificare gli eventi manifesti nei computer che non contengono il provider. Per informazioni dettagliate, vedere la funzione [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) .

In questa versione sono state aggiunte le funzioni seguenti:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

In questa versione sono state aggiunte le strutture seguenti:

-   [**\_ID evento \_ classico**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**Abilita \_ parametri di traccia \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**\_Stack di elementi estesi evento \_ \_ \_ Trace32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**\_Stack di elementi estesi evento \_ \_ \_ TRACE64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_intestazione filtro \_ evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_informazioni sul filtro del provider \_**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

In questa versione sono state aggiunte le enumerazioni seguenti:

-   [**\_classe di informazioni di traccia \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

In questa versione sono state aggiunte le classi MOF seguenti:

-   [**StackWalk**](stackwalk.md)
-   [**\_Evento StackWalk**](stackwalk-event.md)

 

 
