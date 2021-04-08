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
# <a name="capture-a-type-2-dv-file"></a>Acquisire un file DV di tipo 2

Un file AVI DV di tipo 2 ha due flussi, uno contenente video DV e un altro che contiene audio. Per acquisire un file di tipo 2 durante l'anteprima, utilizzare il grafico filtro illustrato nel diagramma seguente.

![acquisizione di tipo 2 con anteprima](images/dv2-cap.png)

Questo grafico è quasi uguale al grafico per l'acquisizione di tipo 1 (vedere [acquisire un file DV di tipo 1](capture-a-type-1-dv-file.md)). Tuttavia, il flusso di acquisizione passa attraverso il filtro della [barra di divisione DV](dv-splitter-filter.md) prima di raggiungere il filtro [Mux AVI](avi-mux-filter.md) . Il mux di AVI riceve quindi due flussi, un flusso audio e un flusso video codificato in formato DV.

Compilare questo grafico come segue:


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



1.  Creare il separatore DV e aggiungerlo al grafico del filtro.
2.  Chiamare [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) per connettere il filtro Mux AVI al filtro del writer di file.
3.  Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione Msdv alla barra di divisione DV. Questa chiamata connette anche uno dei pin di output della barra di divisione DV al Mux AVI.
4.  Chiamare nuovamente RenderStream per connettere l'altro pin della barra di divisione DV al Mux AVI.
5.  Chiamare RenderStream una terza volta per eseguire il rendering del flusso di anteprima. Ignorare questo passaggio se non si desidera visualizzare in anteprima il video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



