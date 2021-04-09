---
description: In questo argomento vengono illustrate alcune funzioni helper per la connessione di filtri DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Connetti due filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124869"
---
# <a name="connect-two-filters"></a><span data-ttu-id="2ea50-103">Connetti due filtri</span><span class="sxs-lookup"><span data-stu-id="2ea50-103">Connect Two Filters</span></span>

<span data-ttu-id="2ea50-104">In questo argomento vengono illustrate alcune funzioni helper per la connessione di filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2ea50-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="2ea50-105">Per connettere due filtri, è necessario trovare un pin di output non connesso sul filtro upstream e un pin di input non connesso sul filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="2ea50-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="2ea50-106">Se sono già presenti puntatori a entrambi i pin, chiamare il metodo [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) per connetterli.</span><span class="sxs-lookup"><span data-stu-id="2ea50-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="2ea50-107">Se i pin non possono connettersi direttamente tra loro, il metodo **IGraphBuilder:: Connect** potrebbe inserire filtri aggiuntivi per completare la connessione.</span><span class="sxs-lookup"><span data-stu-id="2ea50-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="2ea50-108">Per ulteriori informazioni, vedere la pagina relativa alla [connessione intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="2ea50-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="2ea50-109">Se è presente un puntatore ai filtri, ma non ai pin, è necessario usare il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per trovare i pin.</span><span class="sxs-lookup"><span data-stu-id="2ea50-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="2ea50-110">(Vedere [enumerazione dei pin](enumerating-pins.md)). Questa tecnica è illustrata nelle funzioni helper di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2ea50-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="2ea50-111">Pin di output da filtrare</span><span class="sxs-lookup"><span data-stu-id="2ea50-111">Output Pin to Filter</span></span>

<span data-ttu-id="2ea50-112">La funzione seguente accetta due parametri: un puntatore a un pin di output e un puntatore a un filtro.</span><span class="sxs-lookup"><span data-stu-id="2ea50-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="2ea50-113">La funzione connette il pin di output al primo pin di input disponibile sul filtro.</span><span class="sxs-lookup"><span data-stu-id="2ea50-113">The function connects the output pin to the first available input pin on the filter.</span></span>


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



<span data-ttu-id="2ea50-114">Questa funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ea50-114">This function does the following:</span></span>

1.  <span data-ttu-id="2ea50-115">Chiama la `FindUnconnectedPin` funzione per ottenere un pin di input non connesso.</span><span class="sxs-lookup"><span data-stu-id="2ea50-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="2ea50-116">Questa funzione è illustrata nell'argomento [trovare un PIN non connesso in un filtro](find-an-unconnected-pin-on-a-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2ea50-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="2ea50-117">Chiama [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) per connettere i due pin.</span><span class="sxs-lookup"><span data-stu-id="2ea50-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="2ea50-118">Filtrare al pin di input</span><span class="sxs-lookup"><span data-stu-id="2ea50-118">Filter to Input Pin</span></span>

<span data-ttu-id="2ea50-119">La funzione successiva accetta un puntatore a un filtro e un puntatore a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="2ea50-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="2ea50-120">Connette il pin di input al primo pin di output disponibile sul filtro.</span><span class="sxs-lookup"><span data-stu-id="2ea50-120">It connects the input pin to the first available output pin on the filter.</span></span>


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a><span data-ttu-id="2ea50-121">Filtrare per filtrare</span><span class="sxs-lookup"><span data-stu-id="2ea50-121">Filter to Filter</span></span>

<span data-ttu-id="2ea50-122">La terza funzione accetta un puntatore a un filtro upstream e un puntatore a un filtro downstream e tenta di connettere entrambi i filtri.</span><span class="sxs-lookup"><span data-stu-id="2ea50-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2ea50-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ea50-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ea50-124">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="2ea50-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="2ea50-125">**ICaptureGraphBuilder2:: RenderStream**</span><span class="sxs-lookup"><span data-stu-id="2ea50-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



