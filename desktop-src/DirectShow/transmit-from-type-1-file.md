---
description: Trasmissione da un file di tipo 1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Trasmissione da un file di tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050166"
---
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="e0985-103">Trasmissione da un file di tipo 1</span><span class="sxs-lookup"><span data-stu-id="e0985-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="e0985-104">Per trasmettere un file di tipo 1 durante l'anteprima del file, usare il grafico di filtro illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="e0985-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![tipo-1 trasmesso con anteprima](images/dv1-transmit.png)

<span data-ttu-id="e0985-106">I filtri in questo grafico includono:</span><span class="sxs-lookup"><span data-stu-id="e0985-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="e0985-107">Il [separatore AVI](avi-splitter-filter.md) analizza il file AVI.</span><span class="sxs-lookup"><span data-stu-id="e0985-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="e0985-108">Per un file DV di tipo 1, il pin di output fornisce esempi DV con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="e0985-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="e0985-109">Il filtro del [Pin Tee infinito](infinite-pin-tee-filter.md) suddivide il DV con interfoliazione in un flusso di trasmissione e un flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="e0985-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="e0985-110">Entrambi i flussi contengono gli stessi dati con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="e0985-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="e0985-111">(Questo grafico usa il Pin Tee infinito anziché il [Tee intelligente](smart-tee-filter.md), perché non vi è alcun rischio di eliminare i frame durante la lettura da un file, come avviene con l'acquisizione in tempo reale).</span><span class="sxs-lookup"><span data-stu-id="e0985-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="e0985-112">La [barra di divisione DV](dv-splitter-filter.md) suddivide il flusso con interfoliazione in un flusso video DV, decodificato dal [decodificatore video DV](dv-video-decoder-filter.md)e da un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="e0985-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="e0985-113">Entrambi i flussi vengono renderizzati per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="e0985-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="e0985-114">Compilare questo grafico come segue:</span><span class="sxs-lookup"><span data-stu-id="e0985-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  <span data-ttu-id="e0985-115">Chiamare [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere il filtro di origine al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="e0985-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="e0985-116">Creare il separatore AVI e l'infinito Pin Tee e aggiungerli al grafico.</span><span class="sxs-lookup"><span data-stu-id="e0985-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="e0985-117">Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di origine al separatore AVI.</span><span class="sxs-lookup"><span data-stu-id="e0985-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="e0985-118">Specificare MEDIATYPE \_ con interfoliazione per assicurarsi che il metodo non riesca se il file di origine non è un file DV di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="e0985-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="e0985-119">In tal caso, è possibile eseguire il backup e tentare di compilare invece un grafo di trasmissione di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="e0985-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="e0985-120">Chiamare di nuovo **RenderStream** per instradare il flusso con interfoliazione dal separatore AVI al tee infinito del PIN</span><span class="sxs-lookup"><span data-stu-id="e0985-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="e0985-121">Chiamare RenderStream una terza volta per indirizzare un flusso dal tee infinito al filtro MSDV per la trasmissione al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0985-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="e0985-122">Chiamare **RenderStream** un'ultima volta per compilare la sezione di anteprima del grafo.</span><span class="sxs-lookup"><span data-stu-id="e0985-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="e0985-123">Se non si desidera visualizzare l'anteprima, connettere semplicemente l'origine file al filtro MSDV:</span><span class="sxs-lookup"><span data-stu-id="e0985-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="e0985-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0985-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0985-125">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e0985-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



