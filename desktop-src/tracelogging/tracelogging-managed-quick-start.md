---
title: Avvio rapido gestiti TraceLogging
description: Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice gestito.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329575"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="66226-103">Avvio rapido gestiti TraceLogging</span><span class="sxs-lookup"><span data-stu-id="66226-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="66226-104">Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice gestito.</span><span class="sxs-lookup"><span data-stu-id="66226-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66226-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="66226-105">Prerequisites</span></span>

-   <span data-ttu-id="66226-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="66226-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="66226-107">SimpleTraceLoggingExample. cs</span><span class="sxs-lookup"><span data-stu-id="66226-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="66226-108">Questo esempio illustra come registrare gli eventi Tracelogging senza dover creare manualmente un file XML del manifesto di strumentazione separato.</span><span class="sxs-lookup"><span data-stu-id="66226-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a><span data-ttu-id="66226-109">Creare il EventSource</span><span class="sxs-lookup"><span data-stu-id="66226-109">Create the EventSource</span></span>

<span data-ttu-id="66226-110">Prima di poter registrare gli eventi, è necessario creare un'istanza della classe EventSource.</span><span class="sxs-lookup"><span data-stu-id="66226-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="66226-111">Il primo parametro del costruttore identifica il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="66226-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="66226-112">Il provider viene registrato automaticamente come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="66226-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="66226-113">L'istanza è statica perché nell'applicazione deve essere presente solo un'istanza di un provider specifico alla volta.</span><span class="sxs-lookup"><span data-stu-id="66226-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="66226-114">Registra eventi Tracelogging</span><span class="sxs-lookup"><span data-stu-id="66226-114">Log Tracelogging events</span></span>

<span data-ttu-id="66226-115">Dopo la creazione del provider, il seguente codice dell'esempio precedente registra un evento semplice.</span><span class="sxs-lookup"><span data-stu-id="66226-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="66226-116">Registrare i dati del payload dell'evento strutturato</span><span class="sxs-lookup"><span data-stu-id="66226-116">Log structured event payload data</span></span>

<span data-ttu-id="66226-117">È possibile definire dati di payload strutturati che vengono registrati con l'evento.</span><span class="sxs-lookup"><span data-stu-id="66226-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="66226-118">Fornire dati di payload strutturati come tipo anonimo o come istanza di una classe che è stata annotata con l' `[EventData]` attributo, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="66226-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="66226-119">È necessario aggiungere l' `[EventData]` attributo alle classi di payload di eventi definite come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="66226-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="66226-120">L'attributo sostituisce la necessità di creare manualmente un file manifesto per descrivere i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="66226-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="66226-121">A questo punto, è sufficiente passare un'istanza della classe al Metodo EventSource. Write () per registrare l'evento e i dati di payload corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="66226-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="66226-122">Riepilogo e passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="66226-122">Summary and next steps</span></span>

<span data-ttu-id="66226-123">Vedere [registrare e visualizzare gli eventi TraceLogging](tracelogging-record-and-display-tracelogging-events.md) per informazioni su come acquisire e visualizzare i dati di TraceLogging usando le versioni interne più recenti di Windows Performance Tools (WPT).</span><span class="sxs-lookup"><span data-stu-id="66226-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="66226-124">Per esempi più TraceLogging gestiti, vedere [esempi di Tracelogging .NET](tracelogging-net-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="66226-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




