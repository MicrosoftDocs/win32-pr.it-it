---
description: Elenca gli elementi utilizzati con la traccia eventi.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Riferimento traccia eventi
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980575"
---
# <a name="event-tracing-reference"></a><span data-ttu-id="2fff9-103">Riferimento traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2fff9-103">Event Tracing Reference</span></span>

<span data-ttu-id="2fff9-104">Per scrivere applicazioni che incorporano la traccia eventi, usare gli elementi di programmazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fff9-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="2fff9-105">Enumerazioni di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2fff9-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="2fff9-106">Funzioni di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2fff9-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="2fff9-107">Interfacce di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2fff9-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="2fff9-108">Strutture di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2fff9-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="2fff9-109">Costanti di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="2fff9-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="2fff9-110">Per informazioni dettagliate sugli esempi che usano questi elementi di programmazione, vedere [esempi di traccia eventi](event-tracing-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2fff9-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="2fff9-111">Questa sezione contiene anche informazioni su:</span><span class="sxs-lookup"><span data-stu-id="2fff9-111">This section also contains information on:</span></span>

-   <span data-ttu-id="2fff9-112">[Strumenti](event-tracing-tools.md) forniti da ETW</span><span class="sxs-lookup"><span data-stu-id="2fff9-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="2fff9-113">[Definizioni di classi MOF](event-tracing-mof-classes.md) per gli eventi del kernel</span><span class="sxs-lookup"><span data-stu-id="2fff9-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="2fff9-114">[Qualificatori della classe MOF](event-tracing-mof-qualifiers.md) utilizzati durante la definizione delle classi di evento</span><span class="sxs-lookup"><span data-stu-id="2fff9-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="2fff9-115">Elaborare tracce ETW nel codice .NET</span><span class="sxs-lookup"><span data-stu-id="2fff9-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="2fff9-116">È anche possibile usare l' [API .NET TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) per analizzare le tracce ETW per le applicazioni e altri componenti software.</span><span class="sxs-lookup"><span data-stu-id="2fff9-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="2fff9-117">Questa API viene utilizzata internamente in Microsoft per analizzare i dati ETW prodotti dal sistema ingegneristico Windows e viene inoltre utilizzata per potenziare diverse tabelle in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="2fff9-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="2fff9-118">Questa API è disponibile come pacchetto NuGet.</span><span class="sxs-lookup"><span data-stu-id="2fff9-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="2fff9-119">Per altre informazioni, vedi [questo articolo](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="2fff9-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
