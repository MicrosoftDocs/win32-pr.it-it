---
description: Informazioni su Filter Graph Manager
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Informazioni su Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522241"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="f9368-103">Informazioni su Filter Graph Manager</span><span class="sxs-lookup"><span data-stu-id="f9368-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="f9368-104">[Filter Graph Manager](filter-graph-manager.md) è un oggetto com che controlla i filtri in un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="f9368-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="f9368-105">Esegue numerose funzioni, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9368-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="f9368-106">Coordinamento dei cambiamenti di stato tra i filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="f9368-107">Creazione di un orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f9368-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="f9368-108">Comunicazione degli eventi di nuovo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9368-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="f9368-109">Metodi che consentono alle applicazioni di compilare il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="f9368-110">Ognuna di queste funzioni è descritta brevemente qui.</span><span class="sxs-lookup"><span data-stu-id="f9368-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="f9368-111">I dettagli sono disponibili altrove nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="f9368-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="f9368-112">**Modifiche dello stato**.</span><span class="sxs-lookup"><span data-stu-id="f9368-112">**State changes**.</span></span> <span data-ttu-id="f9368-113">Le modifiche di stato all'interno dei filtri devono essere eseguite in un ordine specifico.</span><span class="sxs-lookup"><span data-stu-id="f9368-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="f9368-114">Pertanto, l'applicazione non rilascia i comandi di modifica dello stato direttamente ai filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="f9368-115">Al contrario, fornisce un unico comando al gestore del grafo del filtro, che distribuisce il comando a ognuno dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="f9368-116">La ricerca funziona in modo analogo: l'applicazione fornisce un comando seek a Filter Graph Manager, che lo distribuisce ai filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="f9368-117">**Clock di riferimento**.</span><span class="sxs-lookup"><span data-stu-id="f9368-117">**Reference clock**.</span></span> <span data-ttu-id="f9368-118">Tutti i filtri nel grafico utilizzano lo stesso clock, denominato *clock di riferimento*.</span><span class="sxs-lookup"><span data-stu-id="f9368-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="f9368-119">L'orologio di riferimento garantisce che tutti i flussi siano sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="f9368-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="f9368-120">L'ora in cui deve essere eseguito il rendering di un frame video o di un campione audio è denominata *ora presentazione*.</span><span class="sxs-lookup"><span data-stu-id="f9368-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="f9368-121">Il tempo di presentazione viene misurato in relazione all'orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f9368-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="f9368-122">Il gestore del grafico del filtro sceglie un orologio di riferimento, in genere l'orologio sulla scheda audio o il clock di sistema.</span><span class="sxs-lookup"><span data-stu-id="f9368-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="f9368-123">**Eventi Graph**.</span><span class="sxs-lookup"><span data-stu-id="f9368-123">**Graph events**.</span></span> <span data-ttu-id="f9368-124">Filter Graph Manager usa una coda degli eventi per informare l'applicazione degli eventi che si verificano nel grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="f9368-125">Questo meccanismo è simile a un ciclo di messaggi di Windows.</span><span class="sxs-lookup"><span data-stu-id="f9368-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="f9368-126">**Metodi di creazione di grafici**.</span><span class="sxs-lookup"><span data-stu-id="f9368-126">**Graph-building methods**.</span></span> <span data-ttu-id="f9368-127">Filter Graph Manager fornisce metodi che consentono all'applicazione di aggiungere filtri al grafo, connettere filtri ad altri filtri e disconnettere i filtri.</span><span class="sxs-lookup"><span data-stu-id="f9368-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="f9368-128">Una funzione non gestita dal gestore del grafo del filtro è lo stato di trasferimento dei dati da un filtro a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="f9368-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="f9368-129">Questa operazione viene eseguita dai filtri, tramite le connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="f9368-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="f9368-130">L'elaborazione avviene sempre in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="f9368-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="f9368-131">I filtri sono sempre a thread libero, risiedono nello stesso processo di gestione del grafo dei filtri e vengono caricati dai server in-process.</span><span class="sxs-lookup"><span data-stu-id="f9368-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="f9368-132">Pertanto, le chiamate al metodo non vengono sottoposte a marshalling tra i filtri o tra i filtri e il gestore del grafo del filtro.</span><span class="sxs-lookup"><span data-stu-id="f9368-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f9368-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9368-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9368-134">Flusso di dati nel grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="f9368-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="f9368-135">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f9368-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f9368-136">Impostazione del clock del grafico</span><span class="sxs-lookup"><span data-stu-id="f9368-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="f9368-137">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f9368-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



