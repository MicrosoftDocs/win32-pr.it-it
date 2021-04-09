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
# <a name="capture-dv-to-uncompressed-rgb"></a>Acquisisci DV in RGB non compresso

Questo esempio illustra come acquisire DV dalla videocamera e salvarla in un file come RGB non compresso durante la visualizzazione in anteprima. Usare il grafico di filtro illustrato nel diagramma seguente.

![acquisizione di RGB non compresso in un file](images/dv-rgb-cap.png)

Il filtro della barra di divisione DV suddivide il video/audio con interfoliazione in flussi video e audio distinti. il video con codifica DV passa al filtro del [decodificatore video DV](dv-video-decoder-filter.md) , che restituisce il video RGB non compresso. Il video RGB viene instradato tramite il filtro Smart Tee al filtro Mux AVI (per l'acquisizione) e al renderer video (per l'anteprima). Nel frattempo, il flusso audio dalla barra di divisione DV passa attraverso il filtro di Pin Tee infinito ai Mux AVI e al renderer audio. Filter Graph Manager mantiene tutti questi flussi sincronizzati, usando i timestamp degli esempi e l'orologio di riferimento del grafo.

Questo grafico potrebbe sembrare inutilmente complicato, ma garantisce che il flusso video con codifica DV venga decodificato una sola volta, riducendo al minimo i requisiti della CPU. Si noti anche che il video passa attraverso il filtro Smart Tee mentre l'audio passa attraverso il filtro di Pin Tee infinito. Il tee intelligente può eliminare i frame di anteprima per migliorare le prestazioni di acquisizione, che è consigliabile per i video, ma non per l'audio, in cui i campioni eliminati sono estremamente evidenti. Inoltre, dato che l'audio richiede una larghezza di banda molto inferiore rispetto a quella del video, è possibile che l'audio venga eliminato in modo relativamente ridotto.

È necessario compilare questo grafico una sezione alla volta, ma il metodo RenderStream può comunque essere utile. Usare il codice seguente:


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



È necessario creare il separatore DV, il decodificatore video DV, il tee intelligente e i filtri per pin a infinito, quindi aggiungerli al grafico dei filtri. Per brevità, questi passaggi vengono omessi dal codice precedente. Questo esempio usa il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) per trovare i pin di acquisizione e di anteprima nel filtro Smart Tee; l'acquisizione è sempre il pin di output 0 e l'anteprima è il pin di output 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



