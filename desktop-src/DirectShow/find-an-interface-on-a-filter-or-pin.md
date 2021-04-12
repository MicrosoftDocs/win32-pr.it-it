---
description: Trovare un'interfaccia su un filtro o un pin
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Trovare un'interfaccia su un filtro o un pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225311"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a><span data-ttu-id="88dfb-103">Trovare un'interfaccia su un filtro o un pin</span><span class="sxs-lookup"><span data-stu-id="88dfb-103">Find an Interface on a Filter or Pin</span></span>

<span data-ttu-id="88dfb-104">Per molte operazioni in DirectShow, l'applicazione chiama i metodi in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="88dfb-104">For many operations in DirectShow, the application calls methods on the Filter Graph Manager.</span></span> <span data-ttu-id="88dfb-105">In alcune situazioni, tuttavia, l'applicazione deve chiamare un metodo direttamente su un filtro o un PIN.</span><span class="sxs-lookup"><span data-stu-id="88dfb-105">In some situations, however, the application must call a method directly on a filter or pin.</span></span> <span data-ttu-id="88dfb-106">Molti filtri, ad esempio, espongono interfacce specializzate che vengono usate per configurare il filtro.</span><span class="sxs-lookup"><span data-stu-id="88dfb-106">For example, many filters expose specialized interfaces that are used to configure the filter.</span></span>

<span data-ttu-id="88dfb-107">Nel caso di un'interfaccia di filtro, è possibile che si disponga già di un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.</span><span class="sxs-lookup"><span data-stu-id="88dfb-107">In the case of a filter interface, you might already have a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="88dfb-108">In tal caso, usare semplicemente **QueryInterface** per ottenere l'altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="88dfb-108">In that case, simply use **QueryInterface** to get the other interface.</span></span> <span data-ttu-id="88dfb-109">Tuttavia, è possibile che alcuni filtri vengano aggiunti al grafico dal gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="88dfb-109">But some filters might be added to the graph by the Filter Graph Manager.</span></span> <span data-ttu-id="88dfb-110">Per informazioni dettagliate, vedere [connessione intelligente](intelligent-connect.md). In tal caso, usare l'interfaccia [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) per scorrere in ciclo tutti i filtri nel grafico ed eseguire una query su ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="88dfb-110">(For details, see [Intelligent Connect](intelligent-connect.md).) In that case, use the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface to loop through all the filters in the graph, and query each one in turn.</span></span> <span data-ttu-id="88dfb-111">Nella funzione seguente viene illustrato quanto segue:</span><span class="sxs-lookup"><span data-stu-id="88dfb-111">The following function demonstrates this:</span></span>


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="88dfb-112">Per trovare un'interfaccia su un PIN, usare l'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) per scorrere in ciclo i pin di un filtro.</span><span class="sxs-lookup"><span data-stu-id="88dfb-112">To find an interface on a pin, use the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on a filter.</span></span> <span data-ttu-id="88dfb-113">La funzione seguente mostra come eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="88dfb-113">The following function shows how to do this:</span></span>


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="88dfb-114">La funzione successiva cerca un'interfaccia su un filtro o un PIN:</span><span class="sxs-lookup"><span data-stu-id="88dfb-114">The next function searches for an interface on a filter or a pin:</span></span>


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="88dfb-115">Si noti che tutte le funzioni mostrate qui si arrestano al primo **QueryInterface** riuscito.</span><span class="sxs-lookup"><span data-stu-id="88dfb-115">Note that all of the functions shown here stop at the first successful **QueryInterface**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88dfb-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88dfb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88dfb-117">Enumerazione dei filtri</span><span class="sxs-lookup"><span data-stu-id="88dfb-117">Enumerating Filters</span></span>](enumerating-filters.md)
</dt> <dt>

[<span data-ttu-id="88dfb-118">Enumerazione dei pin</span><span class="sxs-lookup"><span data-stu-id="88dfb-118">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="88dfb-119">**ICaptureGraphBuilder2::FindInterface**</span><span class="sxs-lookup"><span data-stu-id="88dfb-119">**ICaptureGraphBuilder2::FindInterface**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



