---
description: Trasporti
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Trasporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313402"
---
# <a name="transports"></a><span data-ttu-id="20e89-103">Trasporti</span><span class="sxs-lookup"><span data-stu-id="20e89-103">Transports</span></span>

<span data-ttu-id="20e89-104">Per spostare i dati multimediali tramite il grafico dei filtri, un filtro DirectShow deve supportare uno dei diversi protocolli possibili.</span><span class="sxs-lookup"><span data-stu-id="20e89-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="20e89-105">Questi protocolli sono detti trasporti.</span><span class="sxs-lookup"><span data-stu-id="20e89-105">These protocols are called transports.</span></span> <span data-ttu-id="20e89-106">Quando due filtri si connettono, devono supportare lo stesso trasporto; in caso contrario, non possono scambiare dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="20e89-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="20e89-107">In genere, un trasporto richiede che uno dei pin supporti una determinata interfaccia.</span><span class="sxs-lookup"><span data-stu-id="20e89-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="20e89-108">Quando i filtri si connettono, un pin esegue una query sull'altro per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="20e89-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="20e89-109">La maggior parte dei filtri DirectShow consente di mantenere i dati multimediali nella memoria principale e di distribuirla ad altri filtri tra connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="20e89-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="20e89-110">Questo tipo di trasporto è denominato trasporto di memoria locale.</span><span class="sxs-lookup"><span data-stu-id="20e89-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="20e89-111">Sebbene il trasporto di memoria locale sia il trasporto più comune in DirectShow, non tutti i filtri lo usano.</span><span class="sxs-lookup"><span data-stu-id="20e89-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="20e89-112">Ad esempio, alcuni filtri inviano i dati multimediali lungo un percorso hardware e usano solo pin per fornire informazioni sul controllo.</span><span class="sxs-lookup"><span data-stu-id="20e89-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="20e89-113">Vedere ad esempio l'interfaccia [**iOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .</span><span class="sxs-lookup"><span data-stu-id="20e89-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="20e89-114">DirectShow definisce due meccanismi per il trasporto di memoria locale, il modello push e il modello pull.</span><span class="sxs-lookup"><span data-stu-id="20e89-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="20e89-115">Nel modello push un filtro di origine genera dati e li recapita al filtro successivo downstream.</span><span class="sxs-lookup"><span data-stu-id="20e89-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="20e89-116">Tale filtro riceve i dati in modo passivo, li elabora e li invia a valle.</span><span class="sxs-lookup"><span data-stu-id="20e89-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="20e89-117">Nel modello pull il filtro di origine è connesso a un filtro del parser.</span><span class="sxs-lookup"><span data-stu-id="20e89-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="20e89-118">Il filtro del parser richiede i dati dal filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="20e89-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="20e89-119">Il filtro di origine risponde alle richieste tramite la distribuzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="20e89-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="20e89-120">Il modello push usa l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e il modello pull usa l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="20e89-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="20e89-121">Il modello push è più comune del modello pull.</span><span class="sxs-lookup"><span data-stu-id="20e89-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="20e89-122">Gli articoli che seguono presuppongono quindi un modello push.</span><span class="sxs-lookup"><span data-stu-id="20e89-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="20e89-123">Nell'ultimo articolo di questa sezione, [modello pull](pull-model.md), viene descritto il modo in cui l'interfaccia **IAsyncReader** differisce da **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="20e89-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20e89-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20e89-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e89-125">Flusso di dati nel grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="20e89-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



