---
description: In questa sezione vengono descritte le nuove funzionalità aggiunte a Event Tracing for Windows in ogni versione.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Novità di Event Tracing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da1c6f1b54ae8bc4b91bd511bface8569bcf43b2893329b1b0462b46c001724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102021"
---
# <a name="whats-new-in-event-tracing"></a>Novità di Event Tracing

In questa sezione vengono descritte le nuove funzionalità aggiunte a Event Tracing for Windows in ogni versione.

## <a name="windows-10-version-1709"></a>Windows 10, versione 1709

ETW può ora tenere traccia facoltativamente dei file binari per tutti i provider abilitati per la sessione. Il rilevamento si applica retroattivamente per i provider abilitati per la sessione prima della chiamata, nonché per tutti i provider futuri abilitati per la sessione. È ora anche possibile eseguire una query per ottenere il numero massimo di logger di sistema attualmente configurato consentito dal sistema operativo. Per altre informazioni, vedere i valori **TraceProviderBinaryTracking** e **TraceMaxLoggersQuery** dell'enumerazione [**TRACE INFO \_ \_ CLASS,**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) nonché [Recupero di dati aggiuntivi di traccia eventi.](retrieving-additional-event-tracing-data.md)

ETW può ora filtrare gli eventi in base al nome dell'evento. È anche possibile determinare quali eventi ottengono i relativi stack acquisiti. Per altre informazioni, vedere i valori EVENT **\_ FILTER TYPE EVENT \_ \_ \_ NAME**, **EVENT FILTER TYPE \_ \_ \_ STACKWALK \_ NAME** e **EVENT FILTER TYPE \_ \_ \_ STACKWALK LEVEL \_ \_ KW** della struttura [**EVENT FILTER \_ \_ DESCRIPTOR,**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) nonché le strutture [**EVENT FILTER EVENT \_ \_ \_ NAME**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) e [**EVENT FILTER LEVEL \_ \_ \_ KW**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) associate.

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) si basa su ETW e offre un modo semplificato per instrumentare il codice per sviluppatori nativi, .NET e WinRT. TraceLogging consente di includere dati strutturati con eventi, correlare eventi e non richiede un file XML manifesto di strumentazione separato.

[I tratti del provider](provider-traits.md) sono stati aggiunti come metodo per associare più dati a una registrazione di un singolo provider. Possono essere usati per provider basati su manifesto o TraceLogging. Questo include attualmente il supporto per l'aggiunta di un nome provider e/o di un gruppo di provider a una registrazione di un singolo provider. I gruppi di provider sono una nuova funzionalità che consente a più provider ETW di essere controllati in aggregazione dal gruppo a cui appartengono.

Lo stato di acquisizione periodico consente di inviare regolarmente notifiche di stato di acquisizione ai provider. Quando questa opzione è abilitata, le notifiche verranno inviate solo alle registrazioni del provider abilitate in precedenza per la sessione corrente. Ogni provider può definire la propria risposta (se presente) a una notifica. Per informazioni dettagliate sull'implementazione, [**vedere TRACE PERIODIC CAPTURE STATE \_ \_ \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Le funzionalità seguenti sono state aggiunte a Event Tracing in Windows 8.1 e Windows Server 2012 R2.

Funzioni che supportano l'uso di filtri di payload, ambito e analisi dello stack usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger. Per altre informazioni, vedere:

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Vedere anche la documentazione ampiamente modificata per la funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e le strutture [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) usate da queste funzionalità.

Struttura che definisce un predicato del filtro del payload dell'evento che descrive come filtrare in base a un singolo campo in una sessione di traccia usata dalla nuova funzione [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) e una nuova struttura usata dai filtri per l'ID evento e l'analisi dello stack. Per altre informazioni, vedere:

-   [**ID \_ EVENTO \_ FILTRO \_ EVENTI**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**PREDICATO \_ DEL \_ FILTRO DI PAYLOAD**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funzioni che recuperano informazioni sugli eventi presenti nel manifesto del provider. Per altre informazioni, vedere:

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Struttura che definisce una matrice di eventi in un manifesto del provider usato dalla nuova [**funzione TdhEnumerateManifestProviderEvents.**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) Per altre informazioni, vedere:

-   [**INFORMAZIONI \_ SULL'EVENTO \_ DEL PROVIDER**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Le funzionalità seguenti sono state aggiunte a Event Tracing in Windows 8 e Windows Server 2012.

Funzioni che eseguono operazioni su un oggetto di registrazione, forniscono l'analisi del payload degli eventi, forniscono l'esplorazione del provider di traccia, eseguono query sulle impostazioni della sessione di traccia degli eventi ed elaborano un file di traccia rilostato. Per altre informazioni, vedere:

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Interfacce che forniscono informazioni al relogger nel processo di traccia e quando vengono registrati gli eventi, l'accesso ai dati per un evento specifico e l'accesso alle funzionalità di relogger che consentono la manipolazione dei file di log di traccia eventi (ETL). Per altre informazioni, vedere:

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Enumerazioni aggiuntive usate dalle nuove funzioni e interfacce. Per altre informazioni, vedere:

-   [**EVENT \_ INFO \_ CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**CLASSE TRACE \_ QUERY \_ INFO \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

In questa versione sono state aggiunte le funzionalità seguenti:

-   Possibilità per i provider di definire filtri nel manifesto. In Windows Vista i controller possono passare i dati di filtro al provider. Tuttavia, il layout dei dati di filtro non è stato definito nel manifesto, quindi il provider deve usare altri mezzi per fornire la definizione del filtro ai controller. Con questa versione, i provider possono definire la definizione del filtro nel manifesto (vedere l'attributo **filters** del [**tipo complesso ProviderType).**](../wes/eventmanifestschema-providertype-complextype.md) I controller possono quindi usare [**la funzione TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) per determinare la definizione del filtro. I provider che usano filtri devono usare la [**funzione EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) per scrivere l'evento.
-   Possibilità di usare un singolo buffer per raccogliere gli eventi generati su più processori. L'uso di un singolo buffer elimina la visualizzazione degli eventi non in ordine nei computer con più processori. Per informazioni dettagliate, vedere [**la modalità di registrazione EVENT TRACE NO PER PROCESSOR \_ \_ \_ \_ \_ BUFFERING.**](logging-mode-constants.md) Per impostazione predefinita, ETW usa buffer per processore.
-   Possibilità di acquisire un'analisi dello stack per gli eventi. Per abilitare l'analisi dello stack per gli eventi del kernel, vedere la [**funzione TraceSetInformation.**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) Per abilitare l'analisi dello stack per gli eventi utente, vedere il flag **EVENT ENABLE PROPERTY STACK \_ \_ \_ \_ TRACE** per il **membro EnableProperty** di [**ENABLE TRACE \_ \_ PARAMETERS.**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   Possibilità di specificare la modalità di registrazione **EVENT \_ TRACE \_ BUFFERING \_ MODE** o **EVENT TRACE FILE MODE \_ \_ \_ \_ NEWFILE** con la modalità di registrazione **EVENT TRACE PRIVATE \_ \_ \_ LOGGER \_ MODE** (vedere Costanti della [modalità di registrazione).](logging-mode-constants.md)
-   Possibilità di abilitare un provider in modo sincrono. Per impostazione predefinita, i provider sono abilitati in modo asincrono. Per abilitare un provider in modo sincrono, impostare il *parametro Timeout* di [**EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   Possibilità per il controller di richiedere che il provider registri il proprio stato. Per informazioni dettagliate, vedere il flag **EVENT CONTROL CODE CAPTURE \_ \_ \_ \_ STATE** per il *parametro ControlCode* di [**EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   Possibilità per i consumer di formattare i dati degli eventi usando [**la funzione TdhFormatProperty.**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   Possibilità di decodificare gli eventi manifesti nei computer che non contengono il provider. Per informazioni dettagliate, vedere [**la funzione TdhLoadManifest.**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)

In questa versione sono state aggiunte le funzioni seguenti:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

In questa versione sono state aggiunte le strutture seguenti:

-   [**\_ID EVENTO \_ CLASSICO**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**ABILITARE \_ I PARAMETRI DI \_ TRACCIA**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**EVENT \_ EXTENDED \_ ITEM \_ STACK \_ TRACE32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**EVENT \_ EXTENDED \_ ITEM \_ STACK \_ TRACE64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**INTESTAZIONE DEL \_ FILTRO \_ EVENTI**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**PROVIDER \_ FILTER \_ INFO**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

In questa versione sono state aggiunte le enumerazioni seguenti:

-   [**CLASSE TRACE \_ INFO \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

In questa versione sono state aggiunte le classi MOF seguenti:

-   [**StackWalk**](stackwalk.md)
-   [**Evento \_ StackWalk**](stackwalk-event.md)

 

 
