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
# <a name="add-a-filter-by-clsid"></a><span data-ttu-id="6bf32-103">Aggiungere un filtro in base al CLSID</span><span class="sxs-lookup"><span data-stu-id="6bf32-103">Add a Filter by CLSID</span></span>

<span data-ttu-id="6bf32-104">La funzione seguente crea un filtro con un identificatore di classe specificato (CLSID) e lo aggiunge al grafo del filtro:</span><span class="sxs-lookup"><span data-stu-id="6bf32-104">The following function creates a filter with a specified class identifier (CLSID) and adds it to the filter graph:</span></span>


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
> <span data-ttu-id="6bf32-105">In questo esempio viene usata la funzione [SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare il puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="6bf32-105">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>

 

<span data-ttu-id="6bf32-106">La funzione chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il filtro e quindi chiama [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo.</span><span class="sxs-lookup"><span data-stu-id="6bf32-106">The function calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the filter, and then calls [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span> <span data-ttu-id="6bf32-107">L'esempio di codice seguente usa questa funzione per aggiungere il filtro [Mux AVI](avi-mux-filter.md) al grafo:</span><span class="sxs-lookup"><span data-stu-id="6bf32-107">The following code example uses this function to add the [AVI Mux](avi-mux-filter.md) filter to the graph:</span></span>


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



<span data-ttu-id="6bf32-108">Si noti che non è possibile creare alcuni filtri con [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6bf32-108">Note that some filters cannot be created with [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="6bf32-109">Questa situazione si verifica spesso con i filtri che gestiscono altri componenti software.</span><span class="sxs-lookup"><span data-stu-id="6bf32-109">This is often the case with filters that manage other software components.</span></span> <span data-ttu-id="6bf32-110">Ad esempio, il filtro del [compressore AVI](avi-compressor-filter.md) è un wrapper per i codec video e il filtro di [acquisizione video WDM](wdm-video-capture-filter.md) è un wrapper per i driver di acquisizione WDM.</span><span class="sxs-lookup"><span data-stu-id="6bf32-110">For example, the [AVI Compressor](avi-compressor-filter.md) filter is a wrapper for video codecs, and the [WDM Video Capture](wdm-video-capture-filter.md) filter is a wrapper for WDM capture drivers.</span></span> <span data-ttu-id="6bf32-111">Questi filtri devono essere creati utilizzando l' [enumeratore di dispositivo di sistema](system-device-enumerator.md) o il [mapper dei filtri](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="6bf32-111">These filters must be created using either the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="6bf32-112">Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="6bf32-112">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bf32-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bf32-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf32-114">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="6bf32-114">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
