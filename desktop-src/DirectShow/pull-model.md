---
description: Modello pull
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modello pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521345"
---
# <a name="pull-model"></a><span data-ttu-id="89746-103">Modello pull</span><span class="sxs-lookup"><span data-stu-id="89746-103">Pull Model</span></span>

<span data-ttu-id="89746-104">Nell'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) il filtro upstream determina i dati da inviare e inserisce i dati nel filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="89746-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="89746-105">Per alcuni filtri, un modello *pull* è più appropriato.</span><span class="sxs-lookup"><span data-stu-id="89746-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="89746-106">In questo caso il filtro downstream richiede i dati dal filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="89746-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="89746-107">Gli esempi continuano a raggiungere downstream, dal pin di output al pin di input, ma il filtro downstream avvia il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="89746-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="89746-108">Questo tipo di connessione utilizza l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="89746-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="89746-109">L'uso tipico del modello pull è la riproduzione del file.</span><span class="sxs-lookup"><span data-stu-id="89746-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="89746-110">Ad esempio, in un grafico di riproduzione AVI, il filtro di [origine file asincrono](file-source--async--filter.md) esegue operazioni generiche di lettura dei file e recapita i dati come flusso di byte senza informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="89746-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="89746-111">Il filtro [splitter AVI](avi-splitter-filter.md) legge le intestazioni AVI e analizza il flusso in esempi video e audio.</span><span class="sxs-lookup"><span data-stu-id="89746-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="89746-112">Il separatore AVI è in grado di determinare i dati necessari meglio rispetto al filtro di origine file asincrono, quindi usa **IAsyncReader** anziché **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="89746-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="89746-113">Per richiedere dati dal pin di output, il pin di input chiama uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="89746-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="89746-114">**IAsyncReader:: Request**</span><span class="sxs-lookup"><span data-stu-id="89746-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="89746-115">**IAsyncReader::SyncRead**</span><span class="sxs-lookup"><span data-stu-id="89746-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="89746-116">[**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="89746-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="89746-117">Il primo metodo è asincrono per supportare più letture sovrapposte.</span><span class="sxs-lookup"><span data-stu-id="89746-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="89746-118">Le altre sono sincrone.</span><span class="sxs-lookup"><span data-stu-id="89746-118">The others are synchronous.</span></span>

<span data-ttu-id="89746-119">In teoria, qualsiasi filtro può supportare **IAsyncReader**, ma in pratica è progettato per i filtri di origine che si connettono ai filtri del parser.</span><span class="sxs-lookup"><span data-stu-id="89746-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="89746-120">Il parser funziona in modo molto simile a un filtro di origine nel modello push.</span><span class="sxs-lookup"><span data-stu-id="89746-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="89746-121">Quando viene sospesa, viene creato un thread di streaming che estrae i dati dalla connessione **IAsyncReader** e li inserisce a valle.</span><span class="sxs-lookup"><span data-stu-id="89746-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="89746-122">I pin di output usano **IMemInputPin** e il resto del grafo usa il modello push standard.</span><span class="sxs-lookup"><span data-stu-id="89746-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89746-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89746-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89746-124">Flusso di dati nel grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="89746-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



