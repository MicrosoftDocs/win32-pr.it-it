---
description: Trasmissione da un file di tipo 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Trasmissione da un file di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967692"
---
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="be551-103">Trasmissione da un file di tipo 2</span><span class="sxs-lookup"><span data-stu-id="be551-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="be551-104">Per trasmettere un file di tipo 2 durante l'anteprima, usare il grafico di filtro illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="be551-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![tipo 2 trasmesso con anteprima](images/dv2-transmit.png)

<span data-ttu-id="be551-106">Un file di tipo 2 ha due flussi, un flusso audio e un flusso video con codifica DV.</span><span class="sxs-lookup"><span data-stu-id="be551-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="be551-107">Questo grafico usa il filtro [muxer DV](dv-muxer-filter.md) per combinare i flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="be551-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="be551-108">Invia il flusso con interfoliazione al filtro MSDV, ma suddivide nuovamente il flusso per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="be551-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="be551-109">Compilare questo grafico come segue:</span><span class="sxs-lookup"><span data-stu-id="be551-109">Build this graph as follows:</span></span>


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



<span data-ttu-id="be551-110">Questo codice esegue diverse chiamate a **RenderStream**:</span><span class="sxs-lookup"><span data-stu-id="be551-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="be551-111">I primi due connettono il filtro di origine al separatore AVI e al separatore AVI al Mux DV.</span><span class="sxs-lookup"><span data-stu-id="be551-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="be551-112">Nella prima chiamata, il generatore di grafici di acquisizione aggiunge automaticamente il separatore AVI al grafo e connette uno dei pin di output di AVI Splitter alla Mux DV.</span><span class="sxs-lookup"><span data-stu-id="be551-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="be551-113">Nella seconda chiamata, il generatore di grafici di acquisizione trova il secondo pin di output del separatore AVI e lo connette al Mux DV.</span><span class="sxs-lookup"><span data-stu-id="be551-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="be551-114">La terza chiamata a **RenderStream** connette il muxer DV al filtro infinito del Pin Tee.</span><span class="sxs-lookup"><span data-stu-id="be551-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="be551-115">La chiamata successiva connette un flusso dal tee di pin infinito al filtro di acquisizione MSDV.</span><span class="sxs-lookup"><span data-stu-id="be551-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="be551-116">Questo flusso viene trasmesso al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be551-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="be551-117">L'ultima chiamata a **RenderStream** compila la sezione di anteprima del grafo.</span><span class="sxs-lookup"><span data-stu-id="be551-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="be551-118">Se non si desidera visualizzare l'anteprima durante la trasmissione, è possibile omettere il numero infinito di Pin Tee e connettere semplicemente il mux DV al filtro MSDV:</span><span class="sxs-lookup"><span data-stu-id="be551-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="be551-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be551-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be551-120">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="be551-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



