---
description: Enumerazione dei filtri
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Enumerazione dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d584ddf74a13b06e99d9a7e0a34ac802c6da881d87cb163411100ea7772e1df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819664"
---
# <a name="enumerating-filters"></a>Enumerazione dei filtri

Filter Graph Manager supporta il metodo [**IFilterGraph::EnumFilters,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) che enumera tutti i filtri nel grafico dei filtri. Restituisce un puntatore [**all'interfaccia IEnumFilters.**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) Il [**metodo IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) recupera i [**puntatori a interfaccia IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)

Nell'esempio seguente viene illustrata una funzione che enumera i filtri in un grafico e visualizza una finestra di messaggio con il nome di ogni filtro. Usa il [**metodo IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) per recuperare il nome del filtro. Si notino le posizioni in cui la funzione chiama **Release** su un'interfaccia per decrementare il conteggio dei riferimenti.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di oggetti in un filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



