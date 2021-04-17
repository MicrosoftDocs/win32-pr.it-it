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
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="732ff-103">Configurazione e avvio di una sessione di logger privata</span><span class="sxs-lookup"><span data-stu-id="732ff-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="732ff-104">Una sessione di traccia eventi privata è una sessione di traccia eventi in modalità utente eseguita nello stesso processo dei provider di traccia eventi, ovvero la sessione privata e i provider abilitati devono essere tutti nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="732ff-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="732ff-105">Il vantaggio dell'utilizzo di una sessione privata è che la sessione privata non viene conteggiata rispetto al numero massimo di 64 sessioni di traccia eventi eseguite simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="732ff-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="732ff-106">La configurazione e l'avvio di una sessione privata sono simili all'avvio di una normale sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="732ff-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="732ff-107">La differenza è che il membro **WNODE. Guid** della struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) deve contenere il **GUID** del provider e non la sessione e il provider deve avere già registrato il GUID.</span><span class="sxs-lookup"><span data-stu-id="732ff-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="732ff-108">Si noti che se si imposta anche la \_ traccia eventi \_ privata \_ in \_ modalità di registrazione proc, è possibile usare un **GUID** diverso per la sessione e il provider.</span><span class="sxs-lookup"><span data-stu-id="732ff-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="732ff-109">Per informazioni dettagliate sull'avvio di una normale sessione di traccia eventi, vedere [configurazione e avvio di una sessione](configuring-and-starting-an-event-tracing-session.md)di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="732ff-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="732ff-110">Si noti che non è possibile avviare, arrestare o scaricare una sessione di traccia privata da DllMain; è consigliabile eseguire questa operazione nelle routine di inizializzazione e finalizzazione della DLL.</span><span class="sxs-lookup"><span data-stu-id="732ff-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="732ff-111">Da Windows 8.1 a Windows 10, la versione 1607, il payload dell'evento, l'ambito e i filtri di percorso stack possono essere usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**enable \_ trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descrittore filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger.</span><span class="sxs-lookup"><span data-stu-id="732ff-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="732ff-112">Per ulteriori informazioni sui filtri di payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **enable \_ trace \_ Parameters**, **Event \_ Filter \_ descrittor** e [**payload \_ Filter \_ predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .</span><span class="sxs-lookup"><span data-stu-id="732ff-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="732ff-113">A partire da Windows 10, versione 1703, gli utenti con privilegi limitati possono ora avviare una sessione di logger privata nei processi avviati.</span><span class="sxs-lookup"><span data-stu-id="732ff-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="732ff-114">Il provider non deve più essere registrato prima di abilitare o avviare la sessione privata, vale a dire che il provider è "preabilitato" in modo analogo a come sono i provider di sessione non privati.</span><span class="sxs-lookup"><span data-stu-id="732ff-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="732ff-115">È previsto un limite di 8 logger privati a livello di sistema per un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="732ff-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="732ff-116">Per migliorare le prestazioni negli scenari tra processi, è consigliabile usare il filtro per le API di sessione (incluse [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) quando si avvia un logger privato a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="732ff-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="732ff-117">Si noti che gli stessi filtri devono essere passati a tutte le API di sessione.</span><span class="sxs-lookup"><span data-stu-id="732ff-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="732ff-118">Per ulteriori informazioni sui filtri, vedere [**\_ proprietà della traccia eventi \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span><span class="sxs-lookup"><span data-stu-id="732ff-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="732ff-119">Per informazioni dettagliate sull'avvio di una sessione di traccia eventi, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="732ff-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="732ff-120">Per informazioni dettagliate sull'avvio di una sessione del logger di kernel NT, vedere [configurazione e avvio della sessione del logger di kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="732ff-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="732ff-121">Per informazioni dettagliate sull'avvio di una sessione di logger globale, vedere [configurazione e avvio di una sessione di logger globale](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="732ff-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="732ff-122">Per informazioni dettagliate sull'avvio di una sessione di autologger, vedere [configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="732ff-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="732ff-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="732ff-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="732ff-124">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="732ff-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="732ff-125">Configurazione e avvio di una sessione di autologger</span><span class="sxs-lookup"><span data-stu-id="732ff-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="732ff-126">Configurazione e avvio di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="732ff-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="732ff-127">Configurazione e avvio della sessione del logger del kernel NT</span><span class="sxs-lookup"><span data-stu-id="732ff-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="732ff-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="732ff-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="732ff-129">**Abilita \_ parametri di traccia \_**</span><span class="sxs-lookup"><span data-stu-id="732ff-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="732ff-130">**\_proprietà della traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="732ff-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="732ff-131">**\_Proprietà della traccia eventi \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="732ff-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="732ff-132">**\_descrittore filtro eventi \_**</span><span class="sxs-lookup"><span data-stu-id="732ff-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="732ff-133">**\_predicato filtro payload \_**</span><span class="sxs-lookup"><span data-stu-id="732ff-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="732ff-134">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="732ff-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="732ff-135">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="732ff-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="732ff-136">Aggiornamento di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="732ff-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
