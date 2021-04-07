---
description: Gestione grafico filtro
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gestione grafico filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876018"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="a3df2-103">Gestione grafico filtro</span><span class="sxs-lookup"><span data-stu-id="a3df2-103">Filter Graph Manager</span></span>

<span data-ttu-id="a3df2-104">Filter Graph Manager compila e controlla i grafici dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a3df2-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="a3df2-105">Questo oggetto è il componente centrale in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a3df2-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="a3df2-106">Le applicazioni lo usano per compilare e controllare i grafici di filtro.</span><span class="sxs-lookup"><span data-stu-id="a3df2-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="a3df2-107">Filter Graph Manager gestisce anche la sincronizzazione, la notifica degli eventi e altri aspetti del controllo del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="a3df2-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="a3df2-108">Creare questo oggetto chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a3df2-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="a3df2-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="a3df2-109">CLSID</span></span>

<span data-ttu-id="a3df2-110">Sono disponibili due CLSID per la creazione del gestore del grafico dei filtri:</span><span class="sxs-lookup"><span data-stu-id="a3df2-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="a3df2-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="a3df2-111">CLSID</span></span>                      | <span data-ttu-id="a3df2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3df2-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a3df2-113">\_FILTERGRAPH CLSID</span><span class="sxs-lookup"><span data-stu-id="a3df2-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="a3df2-114">Crea il gestore del grafico di filtro in un thread di lavoro condiviso.</span><span class="sxs-lookup"><span data-stu-id="a3df2-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="a3df2-115">\_FILTERGRAPHNOTHREAD CLSID</span><span class="sxs-lookup"><span data-stu-id="a3df2-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="a3df2-116">Crea il gestore del grafico del filtro nel thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3df2-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="a3df2-117">In genere, le applicazioni devono usare CLSID \_ filtergraph.</span><span class="sxs-lookup"><span data-stu-id="a3df2-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="a3df2-118">Entrambi i CLSID creano lo stesso oggetto, ma utilizzano modelli di threading diversi:</span><span class="sxs-lookup"><span data-stu-id="a3df2-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="a3df2-119">CLSID \_ filtergraph crea Filter Graph Manager in un thread di lavoro, che è condiviso da tutte \_ le istanze di filtergraph CLSID nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="a3df2-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="a3df2-120">Il thread invia i messaggi inviati dai filtri e controlla la durata di tutte le finestre create dai filtri.</span><span class="sxs-lookup"><span data-stu-id="a3df2-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="a3df2-121">CLSID \_ FilterGraphNoThread crea il gestore del grafo del filtro nel thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3df2-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="a3df2-122">Se si utilizza questo CLSID, il thread che chiama **CoCreateInstance** deve disporre di un ciclo di messaggi che invia i messaggi; in caso contrario, possono verificarsi deadlock.</span><span class="sxs-lookup"><span data-stu-id="a3df2-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="a3df2-123">Inoltre, prima che il thread dell'applicazione venga chiuso, deve rilasciare Filter Graph Manager e tutti gli oggetti Graph, ad esempio filtri, pin, orologi di riferimento e così via.</span><span class="sxs-lookup"><span data-stu-id="a3df2-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="a3df2-124">Interfacce</span><span class="sxs-lookup"><span data-stu-id="a3df2-124">Interfaces</span></span>

<span data-ttu-id="a3df2-125">Il gestore del grafo del filtro espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3df2-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="a3df2-126">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="a3df2-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="a3df2-127">**IAMStats**</span><span class="sxs-lookup"><span data-stu-id="a3df2-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="a3df2-128">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="a3df2-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="a3df2-129">**IBasicVideo**</span><span class="sxs-lookup"><span data-stu-id="a3df2-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="a3df2-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="a3df2-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="a3df2-131">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="a3df2-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="a3df2-132">**IFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="a3df2-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="a3df2-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="a3df2-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="a3df2-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="a3df2-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="a3df2-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="a3df2-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="a3df2-136">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="a3df2-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="a3df2-137">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="a3df2-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="a3df2-138">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="a3df2-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="a3df2-139">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="a3df2-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="a3df2-140">**IMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="a3df2-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="a3df2-141">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="a3df2-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="a3df2-142">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="a3df2-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="a3df2-143">**IMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="a3df2-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="a3df2-144">**IMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="a3df2-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="a3df2-145">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="a3df2-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="a3df2-146">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="a3df2-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="a3df2-147">**IRegisterServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="a3df2-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="a3df2-148">**IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="a3df2-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="a3df2-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="a3df2-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="a3df2-150">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="a3df2-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="a3df2-151">**IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="a3df2-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="a3df2-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3df2-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3df2-153">Oggetti DirectShow</span><span class="sxs-lookup"><span data-stu-id="a3df2-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



