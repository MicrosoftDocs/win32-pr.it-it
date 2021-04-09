---
description: Acquisisci DV in RGB non compresso
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Acquisisci DV in RGB non compresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123645"
---
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="d2d03-103">Acquisisci DV in RGB non compresso</span><span class="sxs-lookup"><span data-stu-id="d2d03-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="d2d03-104">Questo esempio illustra come acquisire DV dalla videocamera e salvarla in un file come RGB non compresso durante la visualizzazione in anteprima.</span><span class="sxs-lookup"><span data-stu-id="d2d03-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="d2d03-105">Usare il grafico di filtro illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d2d03-105">Use the filter graph shown in the following diagram.</span></span>

![acquisizione di RGB non compresso in un file](images/dv-rgb-cap.png)

<span data-ttu-id="d2d03-107">Il filtro della barra di divisione DV suddivide il video/audio con interfoliazione in flussi video e audio distinti. il video con codifica DV passa al filtro del [decodificatore video DV](dv-video-decoder-filter.md) , che restituisce il video RGB non compresso.</span><span class="sxs-lookup"><span data-stu-id="d2d03-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="d2d03-108">Il video RGB viene instradato tramite il filtro Smart Tee al filtro Mux AVI (per l'acquisizione) e al renderer video (per l'anteprima).</span><span class="sxs-lookup"><span data-stu-id="d2d03-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="d2d03-109">Nel frattempo, il flusso audio dalla barra di divisione DV passa attraverso il filtro di Pin Tee infinito ai Mux AVI e al renderer audio.</span><span class="sxs-lookup"><span data-stu-id="d2d03-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="d2d03-110">Filter Graph Manager mantiene tutti questi flussi sincronizzati, usando i timestamp degli esempi e l'orologio di riferimento del grafo.</span><span class="sxs-lookup"><span data-stu-id="d2d03-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="d2d03-111">Questo grafico potrebbe sembrare inutilmente complicato, ma garantisce che il flusso video con codifica DV venga decodificato una sola volta, riducendo al minimo i requisiti della CPU.</span><span class="sxs-lookup"><span data-stu-id="d2d03-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="d2d03-112">Si noti anche che il video passa attraverso il filtro Smart Tee mentre l'audio passa attraverso il filtro di Pin Tee infinito.</span><span class="sxs-lookup"><span data-stu-id="d2d03-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="d2d03-113">Il tee intelligente può eliminare i frame di anteprima per migliorare le prestazioni di acquisizione, che è consigliabile per i video, ma non per l'audio, in cui i campioni eliminati sono estremamente evidenti.</span><span class="sxs-lookup"><span data-stu-id="d2d03-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="d2d03-114">Inoltre, dato che l'audio richiede una larghezza di banda molto inferiore rispetto a quella del video, è possibile che l'audio venga eliminato in modo relativamente ridotto.</span><span class="sxs-lookup"><span data-stu-id="d2d03-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="d2d03-115">È necessario compilare questo grafico una sezione alla volta, ma il metodo RenderStream può comunque essere utile.</span><span class="sxs-lookup"><span data-stu-id="d2d03-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="d2d03-116">Usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d2d03-116">Use the following code:</span></span>


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



<span data-ttu-id="d2d03-117">È necessario creare il separatore DV, il decodificatore video DV, il tee intelligente e i filtri per pin a infinito, quindi aggiungerli al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="d2d03-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="d2d03-118">Per brevità, questi passaggi vengono omessi dal codice precedente. Questo esempio usa il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) per trovare i pin di acquisizione e di anteprima nel filtro Smart Tee; l'acquisizione è sempre il pin di output 0 e l'anteprima è il pin di output 1.</span><span class="sxs-lookup"><span data-stu-id="d2d03-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2d03-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2d03-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2d03-120">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d2d03-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



