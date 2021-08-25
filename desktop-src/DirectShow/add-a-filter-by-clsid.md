---
description: Aggiungere un filtro in base a CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Aggiungere un filtro in base a CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8306613e5a73ad863b3c16b04529e3e0def12b76fb4e27685db9cb442b6c80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873431"
---
# <a name="add-a-filter-by-clsid"></a>Aggiungere un filtro in base a CLSID

La funzione seguente crea un filtro con un identificatore di classe (CLSID) specificato e lo aggiunge al grafico dei filtri:


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> Questo esempio usa la [funzione SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare il [**puntatore IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)

 

La funzione chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il filtro e quindi chiama [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafico. L'esempio di codice seguente usa questa funzione per aggiungere il filtro [Mux AVI](avi-mux-filter.md) al grafico:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Si noti che alcuni filtri non possono essere creati [**con CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Questo accade spesso con i filtri che gestiscono altri componenti software. Ad esempio, il [filtro AVIClip è](avi-compressor-filter.md) un wrapper per i codec video e il filtro di acquisizione video [WDM](wdm-video-capture-filter.md) è un wrapper per i driver di acquisizione WDM. Questi filtri devono essere creati usando System [Device Enumerator](system-device-enumerator.md) o [Filter Mapper.](filter-mapper.md) Per altre informazioni, vedere [Enumerazione di dispositivi e filtri.](enumerating-devices-and-filters.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche Graph-Building generali](general-graph-building-techniques.md)
</dt> </dl>

 

 
