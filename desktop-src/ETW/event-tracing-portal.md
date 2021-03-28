---
description: Questa documentazione è destinata alle applicazioni in modalità utente che desiderano utilizzare ETW. Per informazioni sulla strumentazione dei driver di dispositivo eseguiti in modalità kernel, vedere la pagina relativa alla traccia del software WPP e aggiunta della traccia eventi ai driver Kernel-Mode in Windows Driver Kit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Event Tracing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349326"
---
# <a name="event-tracing"></a><span data-ttu-id="da34d-104">Event Tracing</span><span class="sxs-lookup"><span data-stu-id="da34d-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="da34d-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="da34d-105">Purpose</span></span>

<span data-ttu-id="da34d-106">Event Tracing for Windows (ETW) fornisce ai programmatori di applicazioni la possibilità di avviare e arrestare le sessioni di traccia eventi, instrumentare un'applicazione per fornire eventi di traccia e utilizzare gli eventi di traccia.</span><span class="sxs-lookup"><span data-stu-id="da34d-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="da34d-107">Gli eventi di traccia contengono un'intestazione di evento e dati definiti dal provider che descrivono lo stato corrente di un'applicazione o di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="da34d-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="da34d-108">È possibile utilizzare gli eventi per eseguire il debug di un'applicazione ed eseguire l'analisi delle prestazioni e della capacità.</span><span class="sxs-lookup"><span data-stu-id="da34d-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="da34d-109">Questa documentazione è destinata alle applicazioni in modalità utente che desiderano utilizzare ETW.</span><span class="sxs-lookup"><span data-stu-id="da34d-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="da34d-110">Per informazioni sulla strumentazione dei driver di dispositivo eseguiti in modalità kernel, vedere la pagina relativa alla [traccia del software WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) e [aggiunta della traccia eventi ai driver Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="da34d-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="da34d-111">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="da34d-111">Where applicable</span></span>

<span data-ttu-id="da34d-112">Utilizzare ETW quando si desidera instrumentare l'applicazione, registrare eventi utente o kernel in un file di log e utilizzare eventi da un file di log o in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="da34d-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="da34d-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="da34d-113">Developer audience</span></span>

<span data-ttu-id="da34d-114">ETW è progettato per gli sviluppatori C e C++ che scrivono applicazioni in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="da34d-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="da34d-115">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="da34d-115">Run-time requirements</span></span>

<span data-ttu-id="da34d-116">ETW è incluso in Microsoft Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="da34d-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="da34d-117">Per informazioni sui sistemi operativi necessari per usare una funzione specifica, vedere la sezione requisiti della documentazione relativa alla funzione.</span><span class="sxs-lookup"><span data-stu-id="da34d-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="da34d-118">Elaborare tracce ETW nel codice .NET</span><span class="sxs-lookup"><span data-stu-id="da34d-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="da34d-119">È possibile usare l' [API .NET TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) per analizzare le tracce ETW per le applicazioni e altri componenti software.</span><span class="sxs-lookup"><span data-stu-id="da34d-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="da34d-120">Questa API viene utilizzata internamente in Microsoft per analizzare i dati ETW prodotti dal sistema ingegneristico Windows e viene inoltre utilizzata per potenziare diverse tabelle in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="da34d-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="da34d-121">Questa API è disponibile come pacchetto NuGet.</span><span class="sxs-lookup"><span data-stu-id="da34d-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="da34d-122">Per altre informazioni, vedi [questo articolo](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="da34d-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="da34d-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="da34d-123">In this section</span></span>



| <span data-ttu-id="da34d-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="da34d-124">Topic</span></span>                                                                     | <span data-ttu-id="da34d-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da34d-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="da34d-126">Novità della traccia eventi</span><span class="sxs-lookup"><span data-stu-id="da34d-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="da34d-127">Nuove funzionalità aggiunte alla traccia eventi in ogni versione.</span><span class="sxs-lookup"><span data-stu-id="da34d-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="da34d-128">Informazioni sulla traccia eventi</span><span class="sxs-lookup"><span data-stu-id="da34d-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="da34d-129">Informazioni generali sull'analisi degli eventi.</span><span class="sxs-lookup"><span data-stu-id="da34d-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="da34d-130">Utilizzo di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="da34d-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="da34d-131">Argomenti correlati alle attività che descrivono come usare l'API ETW.</span><span class="sxs-lookup"><span data-stu-id="da34d-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="da34d-132">Riferimento traccia eventi</span><span class="sxs-lookup"><span data-stu-id="da34d-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="da34d-133">Descrizione dettagliata delle funzioni ETW e di altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="da34d-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
