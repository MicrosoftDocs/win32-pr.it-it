---
description: Acquisire un file DV di tipo 2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Acquisire un file DV di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876078"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="b73dc-103">Acquisire un file DV di tipo 2</span><span class="sxs-lookup"><span data-stu-id="b73dc-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="b73dc-104">Un file AVI DV di tipo 2 ha due flussi, uno contenente video DV e un altro che contiene audio.</span><span class="sxs-lookup"><span data-stu-id="b73dc-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="b73dc-105">Per acquisire un file di tipo 2 durante l'anteprima, utilizzare il grafico filtro illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="b73dc-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![acquisizione di tipo 2 con anteprima](images/dv2-cap.png)

<span data-ttu-id="b73dc-107">Questo grafico è quasi uguale al grafico per l'acquisizione di tipo 1 (vedere [acquisire un file DV di tipo 1](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="b73dc-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="b73dc-108">Tuttavia, il flusso di acquisizione passa attraverso il filtro della [barra di divisione DV](dv-splitter-filter.md) prima di raggiungere il filtro [Mux AVI](avi-mux-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b73dc-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="b73dc-109">Il mux di AVI riceve quindi due flussi, un flusso audio e un flusso video codificato in formato DV.</span><span class="sxs-lookup"><span data-stu-id="b73dc-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="b73dc-110">Compilare questo grafico come segue:</span><span class="sxs-lookup"><span data-stu-id="b73dc-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="b73dc-111">Creare il separatore DV e aggiungerlo al grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="b73dc-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="b73dc-112">Chiamare [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) per connettere il filtro Mux AVI al filtro del writer di file.</span><span class="sxs-lookup"><span data-stu-id="b73dc-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="b73dc-113">Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione Msdv alla barra di divisione DV.</span><span class="sxs-lookup"><span data-stu-id="b73dc-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="b73dc-114">Questa chiamata connette anche uno dei pin di output della barra di divisione DV al Mux AVI.</span><span class="sxs-lookup"><span data-stu-id="b73dc-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="b73dc-115">Chiamare nuovamente RenderStream per connettere l'altro pin della barra di divisione DV al Mux AVI.</span><span class="sxs-lookup"><span data-stu-id="b73dc-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="b73dc-116">Chiamare RenderStream una terza volta per eseguire il rendering del flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b73dc-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="b73dc-117">Ignorare questo passaggio se non si desidera visualizzare in anteprima il video.</span><span class="sxs-lookup"><span data-stu-id="b73dc-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b73dc-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b73dc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b73dc-119">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b73dc-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



