---
description: Aggiungere un filtro in base al CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Aggiungere un filtro in base al CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125325"
---
# <a name="add-a-filter-by-clsid"></a>Aggiungere un filtro in base al CLSID

La funzione seguente crea un filtro con un identificatore di classe specificato (CLSID) e lo aggiunge al grafo del filtro:


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
> In questo esempio viene usata la funzione [SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare il puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .

 

La funzione chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il filtro e quindi chiama [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo. L'esempio di codice seguente usa questa funzione per aggiungere il filtro [Mux AVI](avi-mux-filter.md) al grafo:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Si noti che non è possibile creare alcuni filtri con [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Questa situazione si verifica spesso con i filtri che gestiscono altri componenti software. Ad esempio, il filtro del [compressore AVI](avi-compressor-filter.md) è un wrapper per i codec video e il filtro di [acquisizione video WDM](wdm-video-capture-filter.md) è un wrapper per i driver di acquisizione WDM. Questi filtri devono essere creati utilizzando l' [enumeratore di dispositivo di sistema](system-device-enumerator.md) o il [mapper dei filtri](filter-mapper.md). Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche di Graph-Building generali](general-graph-building-techniques.md)
</dt> </dl>

 

 
