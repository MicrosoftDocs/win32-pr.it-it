---
description: Acquisire un file DV di tipo 1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Acquisire un file DV di tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104565725"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="bcdfe-103">Acquisire un file DV di tipo 1</span><span class="sxs-lookup"><span data-stu-id="bcdfe-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="bcdfe-104">Un file AVI DV di tipo 1 contiene un singolo flusso con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="bcdfe-105">Per acquisire un file di tipo 1 durante l'anteprima, utilizzare il grafico filtro illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![acquisizione di tipo 1 con anteprima](images/dv1-cap.png)

<span data-ttu-id="bcdfe-107">I filtri in questo grafico includono:</span><span class="sxs-lookup"><span data-stu-id="bcdfe-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="bcdfe-108">Il filtro [Smart Tee](smart-tee-filter.md) suddivide il DV con interfoliazione in un flusso di acquisizione e in un flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="bcdfe-109">Entrambi i flussi contengono gli stessi dati con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="bcdfe-110">Il [Mux](avi-mux-filter.md) e il [writer di file](file-writer-filter.md) scrivono il flusso con interfoliazione su disco.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="bcdfe-111">La [barra di divisione DV](dv-splitter-filter.md) suddivide il flusso con interfoliazione in un flusso video DV e un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="bcdfe-112">Entrambi i flussi vengono renderizzati per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="bcdfe-113">Il [decodificatore video DV](dv-video-decoder-filter.md) decodifica il flusso video DV per la visualizzazione in anteprima.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="bcdfe-114">Compilare questo grafico come segue:</span><span class="sxs-lookup"><span data-stu-id="bcdfe-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="bcdfe-115">Chiamare [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) per connettere il filtro Mux AVI al filtro del writer di file.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="bcdfe-116">Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con l'acquisizione della categoria pin della categoria pin \_ \_ per eseguire il rendering del flusso di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="bcdfe-117">Il generatore del grafico di acquisizione inserisce automaticamente il filtro di Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="bcdfe-118">Chiamare nuovamente RenderStream, ma con l'anteprima della categoria pin Category PIN \_ \_ , per eseguire il rendering del flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="bcdfe-119">Ignorare questa chiamata se non si desidera visualizzare in anteprima il video.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="bcdfe-120">Per entrambe le chiamate a RenderStream, il tipo di supporto è MEDIATYPE con \_ interfoliazione, ovvero video DV con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="bcdfe-121">In questo codice, il generatore di grafici di acquisizione aggiunge automaticamente tutti i filtri necessari, ad eccezione del filtro di acquisizione MSDV.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcdfe-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bcdfe-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcdfe-123">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcdfe-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



