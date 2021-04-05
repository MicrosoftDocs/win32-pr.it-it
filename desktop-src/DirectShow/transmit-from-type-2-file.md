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
# <a name="transmit-from-type-2-file"></a>Trasmissione da un file di tipo 2

Per trasmettere un file di tipo 2 durante l'anteprima, usare il grafico di filtro illustrato nel diagramma seguente.

![tipo 2 trasmesso con anteprima](images/dv2-transmit.png)

Un file di tipo 2 ha due flussi, un flusso audio e un flusso video con codifica DV. Questo grafico usa il filtro [muxer DV](dv-muxer-filter.md) per combinare i flussi audio e video. Invia il flusso con interfoliazione al filtro MSDV, ma suddivide nuovamente il flusso per l'anteprima.

Compilare questo grafico come segue:


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



Questo codice esegue diverse chiamate a **RenderStream**:

I primi due connettono il filtro di origine al separatore AVI e al separatore AVI al Mux DV. Nella prima chiamata, il generatore di grafici di acquisizione aggiunge automaticamente il separatore AVI al grafo e connette uno dei pin di output di AVI Splitter alla Mux DV. Nella seconda chiamata, il generatore di grafici di acquisizione trova il secondo pin di output del separatore AVI e lo connette al Mux DV.

La terza chiamata a **RenderStream** connette il muxer DV al filtro infinito del Pin Tee. La chiamata successiva connette un flusso dal tee di pin infinito al filtro di acquisizione MSDV. Questo flusso viene trasmesso al dispositivo. L'ultima chiamata a **RenderStream** compila la sezione di anteprima del grafo.

Se non si desidera visualizzare l'anteprima durante la trasmissione, è possibile omettere il numero infinito di Pin Tee e connettere semplicemente il mux DV al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



