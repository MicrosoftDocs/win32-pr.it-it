---
description: Visualizzazione del televideo standard internazionale
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Visualizzazione del televideo standard internazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344376"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="b3667-103">Visualizzazione del televideo standard internazionale</span><span class="sxs-lookup"><span data-stu-id="b3667-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="b3667-104">Questa funzionalità è stata rimossa da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="b3667-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="b3667-105">È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b3667-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="b3667-106">Il televideo WST (World Standard Teletext) viene codificato nell'intervallo di spaziatura verticale (VBI) del segnale della televisione analogo.</span><span class="sxs-lookup"><span data-stu-id="b3667-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="b3667-107">Il grafico filtro per la visualizzazione in anteprima del televideo è simile al grafico usato per visualizzare le didascalie chiuse.</span><span class="sxs-lookup"><span data-stu-id="b3667-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="b3667-108">Il diagramma seguente illustra il grafico.</span><span class="sxs-lookup"><span data-stu-id="b3667-108">The following diagram illustrates this graph.</span></span>

![grafico di anteprima WST](images/vidcap10.png)

<span data-ttu-id="b3667-110">Questo grafico usa i filtri seguenti per la visualizzazione WST:</span><span class="sxs-lookup"><span data-stu-id="b3667-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="b3667-111">[Convertitore da tee a sink a sink](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="b3667-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="b3667-112">Accetta le informazioni VBI dal filtro di acquisizione e le suddivide in flussi distinti per ognuno dei servizi dati presenti sul segnale.</span><span class="sxs-lookup"><span data-stu-id="b3667-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="b3667-113">[Codec WST](wst-codec-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b3667-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="b3667-114">Decodifica i dati del televideo dagli esempi di VBI.</span><span class="sxs-lookup"><span data-stu-id="b3667-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="b3667-115">[Decodificatore WST](wst-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b3667-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="b3667-116">Converte i dati del televideo e disegna il testo sulle bitmap.</span><span class="sxs-lookup"><span data-stu-id="b3667-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="b3667-117">Il filtro downstream (in questo caso il mixer overlay) sovrappone le bitmap nel video.</span><span class="sxs-lookup"><span data-stu-id="b3667-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="b3667-118">Il metodo **RenderStream** del generatore di grafici di acquisizione non supporta direttamente i filtri WST, quindi l'applicazione deve eseguire alcune operazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="b3667-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="b3667-119">Aggiungere il filtro del mixer sovrapposto al grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="b3667-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="b3667-120">Il codice seguente usa la funzione AddFilterByCLSID descritta in [aggiungere un filtro in base a CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="b3667-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="b3667-121">(AddFilterByCLSID non è un'API DirectShow).</span><span class="sxs-lookup"><span data-stu-id="b3667-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="b3667-122">Connettere il pin di anteprima al filtro renderer video tramite il mixer overlay.</span><span class="sxs-lookup"><span data-stu-id="b3667-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="b3667-123">È possibile usare il metodo **RenderStream** , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b3667-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="b3667-124">Aggiungere il filtro del convertitore Tee/Sink-to-sink al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="b3667-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="b3667-125">Il codice seguente usa la funzione CreateKernelFilter descritta in [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b3667-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="b3667-126">(CreateKernelFilter non è un'API DirectShow).</span><span class="sxs-lookup"><span data-stu-id="b3667-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="b3667-127">Aggiungere il filtro del codec WST al grafico del filtro:</span><span class="sxs-lookup"><span data-stu-id="b3667-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="b3667-128">Chiamare **RenderStream** per connettere il pin VBI del filtro di acquisizione al convertitore Tee/Sink-to-sink e il convertitore Tee/Sink-to-sink al filtro per il codec WST:</span><span class="sxs-lookup"><span data-stu-id="b3667-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="b3667-129">Chiamare nuovamente **RenderStream** per connettere il filtro del codec WST al mixer della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="b3667-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="b3667-130">Il filtro del decodificatore WST viene automaticamente inserito nel grafico.</span><span class="sxs-lookup"><span data-stu-id="b3667-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="b3667-131">Ricordarsi di rilasciare tutte le interfacce del filtro.</span><span class="sxs-lookup"><span data-stu-id="b3667-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="b3667-132">Attualmente, il filtro decodificatore WST non supporta le connessioni al filtro VMR (video Mixing Renderer).</span><span class="sxs-lookup"><span data-stu-id="b3667-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="b3667-133">Pertanto, è necessario utilizzare il filtro renderer video legacy per visualizzare il televideo.</span><span class="sxs-lookup"><span data-stu-id="b3667-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="b3667-134">Se il filtro di acquisizione ha una porta video VBI pin (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), connetterlo al filtro [VBI Surface allocator](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b3667-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="b3667-135">Il grafico non viene eseguito correttamente in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b3667-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="b3667-136">Nell'esempio di codice seguente viene usata la funzione AddFilterByCLSID, descritta in [aggiungere un filtro in base al CLSID](add-a-filter-by-clsid.md)e la funzione FindPinByCategory, descritta in [uso delle categorie di pin](working-with-pin-categories.md).</span><span class="sxs-lookup"><span data-stu-id="b3667-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="b3667-137">(Nessuna delle due funzioni è un'API DirectShow).</span><span class="sxs-lookup"><span data-stu-id="b3667-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="b3667-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3667-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3667-139">Didascalie e televideo chiusi</span><span class="sxs-lookup"><span data-stu-id="b3667-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



