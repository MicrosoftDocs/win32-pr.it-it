---
description: Salvataggio di un grafico di filtro in un file GraphEdit
ms.assetid: f7eeae3c-506b-484c-8fe5-ddd391af5a59
title: Salvataggio di un grafico di filtro in un file GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5fb24c40f11dbeb5dad8b542f0f152449f8951
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304125"
---
# <a name="saving-a-filter-graph-to-a-graphedit-file"></a><span data-ttu-id="5c6f9-103">Salvataggio di un grafico di filtro in un file GraphEdit</span><span class="sxs-lookup"><span data-stu-id="5c6f9-103">Saving a Filter Graph to a GraphEdit File</span></span>

<span data-ttu-id="5c6f9-104">Nell'esempio di codice seguente viene illustrato come salvare un grafico di filtro in un file GraphEdit (con estensione GRF).</span><span class="sxs-lookup"><span data-stu-id="5c6f9-104">The following code example shows how to save a filter graph to a GraphEdit (.grf) file.</span></span> <span data-ttu-id="5c6f9-105">Questa operazione può essere utile per il debug delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5c6f9-105">This can be useful for debugging your applications.</span></span>


```C++
HRESULT SaveGraphFile(IGraphBuilder *pGraph, WCHAR *wszPath) 
{
    const WCHAR wszStreamName[] = L"ActiveMovieGraph"; 
    HRESULT hr;
    
    IStorage *pStorage = NULL;
    hr = StgCreateDocfile(
        wszPath,
        STGM_CREATE | STGM_TRANSACTED | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0, &pStorage);
    if(FAILED(hr)) 
    {
        return hr;
    }

    IStream *pStream;
    hr = pStorage->CreateStream(
        wszStreamName,
        STGM_WRITE | STGM_CREATE | STGM_SHARE_EXCLUSIVE,
        0, 0, &pStream);
    if (FAILED(hr)) 
    {
        pStorage->Release();    
        return hr;
    }

    IPersistStream *pPersist = NULL;
    pGraph->QueryInterface(IID_IPersistStream, (void**)&pPersist);
    hr = pPersist->Save(pStream, TRUE);
    pStream->Release();
    pPersist->Release();
    if (SUCCEEDED(hr)) 
    {
        hr = pStorage->Commit(STGC_DEFAULT);
    }
    pStorage->Release();
    return hr;
}
```



<span data-ttu-id="5c6f9-106">Il codice seguente, ad esempio, compila un grafico di riproduzione file e lo salva in un file denominato Graph. GRF:</span><span class="sxs-lookup"><span data-stu-id="5c6f9-106">For example, the following code builds a file playback graph and saves it to a file named MyGraph.grf:</span></span>


```C++
void __cdecl main(void)
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    CoInitialize(NULL);
    
    // Create the Filter Graph Manager and render a file.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
        IID_IGraphBuilder, reinterpret_cast<void**>(&pGraph));
    hr = pGraph->RenderFile(L"C:\\Video.avi", NULL);

    if (SUCCEEDED(hr))
    {
        hr = SaveGraphFile(pGraph, L"C:\\MyGraph.grf");
    }
    
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="5c6f9-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c6f9-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c6f9-108">Simulazione della creazione di grafici con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="5c6f9-108">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="5c6f9-109">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="5c6f9-109">**StgCreateDocfile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> </dl>

 

 
