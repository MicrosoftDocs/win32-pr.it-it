---
description: Creazione di grafici dinamici
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Creazione di grafici dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304008"
---
# <a name="dynamic-graph-building"></a><span data-ttu-id="59fa1-103">Creazione di grafici dinamici</span><span class="sxs-lookup"><span data-stu-id="59fa1-103">Dynamic Graph Building</span></span>

<span data-ttu-id="59fa1-104">Se è necessario modificare un grafico filtro esistente, è possibile arrestare il grafo, apportare le modifiche e riavviare il grafo.</span><span class="sxs-lookup"><span data-stu-id="59fa1-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="59fa1-105">Questo è in genere l'approccio migliore.</span><span class="sxs-lookup"><span data-stu-id="59fa1-105">This is usually the best approach.</span></span> <span data-ttu-id="59fa1-106">In alcune circostanze, tuttavia, potrebbe essere necessario modificare un grafico mentre è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="59fa1-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="59fa1-107">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="59fa1-107">For example:</span></span>

-   <span data-ttu-id="59fa1-108">L'applicazione inserisce un filtro effetti video durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="59fa1-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="59fa1-109">Un filtro di origine alterna i tipi di supporto a metà, eventualmente richiedendo un nuovo filtro di decompressione.</span><span class="sxs-lookup"><span data-stu-id="59fa1-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="59fa1-110">L'applicazione aggiunge un nuovo flusso video al grafico.</span><span class="sxs-lookup"><span data-stu-id="59fa1-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="59fa1-111">Questi sono tutti esempi di *compilazione dinamica dei grafici*, un termine che copre qualsiasi tipo di modifica a un grafico di filtro mentre il grafo continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="59fa1-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="59fa1-112">La compilazione dinamica dei grafici può essere avviata da un'applicazione o da un filtro nel grafico.</span><span class="sxs-lookup"><span data-stu-id="59fa1-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="59fa1-113">Sono possibili tre scenari distinti:</span><span class="sxs-lookup"><span data-stu-id="59fa1-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="59fa1-114">[Modifiche al formato dinamico](dynamic-format-changes.md): un filtro può modificare i formati A metà, senza dover rimuovere o sostituire alcun filtro.</span><span class="sxs-lookup"><span data-stu-id="59fa1-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="59fa1-115">[Riconnessione dinamica](dynamic-reconnection.md): modifica del grafico mediante l'aggiunta o la rimozione di filtri.</span><span class="sxs-lookup"><span data-stu-id="59fa1-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="59fa1-116">[Catene](filter-chains.md)di filtri: aggiunta, rimozione e controllo di catene di filtri.</span><span class="sxs-lookup"><span data-stu-id="59fa1-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59fa1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59fa1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59fa1-118">Informazioni su DirectShow</span><span class="sxs-lookup"><span data-stu-id="59fa1-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



