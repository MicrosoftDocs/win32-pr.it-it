---
description: Flusso di dati per sviluppatori di filtri
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Flusso di dati per sviluppatori di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049054"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="b1e26-103">Flusso di dati per sviluppatori di filtri</span><span class="sxs-lookup"><span data-stu-id="b1e26-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="b1e26-104">In questa sezione viene descritto in dettaglio il modo in cui i dati vengono spostati attraverso il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="b1e26-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="b1e26-105">Si concentra sul trasporto di memoria locale usando l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) o [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="b1e26-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="b1e26-106">È destinato agli sviluppatori che scrivono filtri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b1e26-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="b1e26-107">Per un'introduzione generale al modo in cui Microsoft DirectShow gestisce il flusso di dati, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="b1e26-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="b1e26-108">Una grande quantità di dati viene spostata attraverso un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="b1e26-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="b1e26-109">Rientra approssimativamente in due categorie: dati multimediali e dati di controllo.</span><span class="sxs-lookup"><span data-stu-id="b1e26-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="b1e26-110">In generale, i dati multimediali viaggiano a valle e i dati di controllo viaggiano a Monte.</span><span class="sxs-lookup"><span data-stu-id="b1e26-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="b1e26-111">I dati multimediali includono i fotogrammi video, gli esempi audio, i pacchetti MPEG e così via che costituiscono un flusso, ma includono anche comandi di scaricamento, notifiche di fine flusso e altri dati che viaggiano con il flusso.</span><span class="sxs-lookup"><span data-stu-id="b1e26-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="b1e26-112">I dati del controllo non fanno parte del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="b1e26-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="b1e26-113">Esempi di dati di controllo sono richieste di controllo della qualità e comandi di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b1e26-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="b1e26-114">Questa sezione contiene gli articoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1e26-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="b1e26-115">Distribuzione di esempi</span><span class="sxs-lookup"><span data-stu-id="b1e26-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="b1e26-116">Elaborazione dei dati</span><span class="sxs-lookup"><span data-stu-id="b1e26-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="b1e26-117">Notifiche di fine flusso</span><span class="sxs-lookup"><span data-stu-id="b1e26-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="b1e26-118">Nuovi segmenti</span><span class="sxs-lookup"><span data-stu-id="b1e26-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="b1e26-119">Flushing</span><span class="sxs-lookup"><span data-stu-id="b1e26-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="b1e26-120">La ricerca</span><span class="sxs-lookup"><span data-stu-id="b1e26-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="b1e26-121">Modifiche al formato dinamico</span><span class="sxs-lookup"><span data-stu-id="b1e26-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="b1e26-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1e26-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1e26-123">Gestione controllo qualità</span><span class="sxs-lookup"><span data-stu-id="b1e26-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="b1e26-124">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="b1e26-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="b1e26-125">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="b1e26-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



