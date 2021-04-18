---
description: Enumerazione dei filtri
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Enumerazione dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de0f979973d339b790b04a8a5d4d98fc52c95c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303968"
---
# <a name="enumerating-filters"></a><span data-ttu-id="a6b0c-103">Enumerazione dei filtri</span><span class="sxs-lookup"><span data-stu-id="a6b0c-103">Enumerating Filters</span></span>

<span data-ttu-id="a6b0c-104">Filter Graph Manager supporta il metodo [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , che enumera tutti i filtri nel grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a6b0c-104">The Filter Graph Manager supports the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method, which enumerates all the filters in the filter graph.</span></span> <span data-ttu-id="a6b0c-105">Restituisce un puntatore all'interfaccia [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) .</span><span class="sxs-lookup"><span data-stu-id="a6b0c-105">It returns a pointer to the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface.</span></span> <span data-ttu-id="a6b0c-106">Il metodo [**IEnumFilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) recupera i puntatori dell'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="a6b0c-106">The [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) method retrieves [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointers.</span></span>

<span data-ttu-id="a6b0c-107">Nell'esempio seguente viene illustrata una funzione che enumera i filtri in un grafico e visualizza una finestra di messaggio con il nome di ogni filtro.</span><span class="sxs-lookup"><span data-stu-id="a6b0c-107">The following example shows a function that enumerates the filters in a graph and displays a message box with each filter's name.</span></span> <span data-ttu-id="a6b0c-108">Usa il metodo [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) per recuperare il nome del filtro.</span><span class="sxs-lookup"><span data-stu-id="a6b0c-108">It uses the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method to retrieve the name of the filter.</span></span> <span data-ttu-id="a6b0c-109">Si notino i punti in cui la funzione chiama **Release** su un'interfaccia per decrementare il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="a6b0c-109">Note the places where the function calls **Release** on an interface to decrement the reference count.</span></span>


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="a6b0c-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6b0c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b0c-111">Enumerazione di oggetti in un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="a6b0c-111">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



