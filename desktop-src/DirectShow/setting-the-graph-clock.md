---
description: Impostazione del clock del grafico
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Impostazione del clock del grafico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303694"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="535b7-103">Impostazione del clock del grafico</span><span class="sxs-lookup"><span data-stu-id="535b7-103">Setting the Graph Clock</span></span>

<span data-ttu-id="535b7-104">Quando si compila un grafico di filtro, il gestore del grafico del filtro sceglie automaticamente un orologio di riferimento per il grafico.</span><span class="sxs-lookup"><span data-stu-id="535b7-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="535b7-105">Tutti i filtri nel grafico vengono sincronizzati con l'orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="535b7-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="535b7-106">In particolare, i filtri renderer utilizzano l'orologio di riferimento per determinare l'ora di presentazione di ogni campione.</span><span class="sxs-lookup"><span data-stu-id="535b7-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="535b7-107">In genere non esiste alcun motivo per cui un'applicazione esegua l'override della scelta dell'orologio di riferimento del gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="535b7-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="535b7-108">Tuttavia, è possibile eseguire questa operazione chiamando il metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) su Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="535b7-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="535b7-109">Questo metodo accetta un puntatore all'interfaccia **IReferenceClock** del clock.</span><span class="sxs-lookup"><span data-stu-id="535b7-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="535b7-110">Chiamare il metodo mentre il grafo viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="535b7-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="535b7-111">Se un filtro fornisce un clock, è possibile ottenere il puntatore **IReferenceClock** chiamando **QueryInterface** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="535b7-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="535b7-112">In alternativa, è possibile implementare un clock di riferimento esterno che non viene fornito da un filtro, purché il clock esterno implementi **IReferenceClock**.</span><span class="sxs-lookup"><span data-stu-id="535b7-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="535b7-113">Nell'esempio seguente viene illustrato come specificare un clock:</span><span class="sxs-lookup"><span data-stu-id="535b7-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="535b7-114">Questo esempio si basa sul presupposto che CreateMyPrivateClock sia una funzione definita dall'applicazione che crea un clock e restituisce un puntatore **IReferenceClock** .</span><span class="sxs-lookup"><span data-stu-id="535b7-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="535b7-115">È anche possibile impostare il grafo del filtro per l'esecuzione senza clock, chiamando **SetSyncSource** con il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="535b7-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="535b7-116">Se non è presente alcun clock, il grafico viene eseguito il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="535b7-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="535b7-117">Senza clock, i filtri renderer non attendono l'ora di presentazione di un campione.</span><span class="sxs-lookup"><span data-stu-id="535b7-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="535b7-118">Ma eseguono il rendering di ogni campione non appena arriva.</span><span class="sxs-lookup"><span data-stu-id="535b7-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="535b7-119">L'impostazione del grafico per l'esecuzione senza un clock è utile se si desidera elaborare i dati in modo rapido, invece di visualizzarne l'anteprima in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="535b7-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="535b7-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="535b7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="535b7-121">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="535b7-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="535b7-122">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="535b7-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="535b7-123">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="535b7-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



