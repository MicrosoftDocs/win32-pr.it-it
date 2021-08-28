---
description: Trasmettere dal file di tipo 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Trasmettere dal file di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315717"
---
# <a name="transmit-from-type-2-file"></a>Trasmettere dal file di tipo 2

Per trasmettere un file di tipo 2 durante l'anteprima, usare il grafico dei filtri illustrato nel diagramma seguente.

![trasmissione di tipo 2 con anteprima](images/dv2-transmit.png)

Un file di tipo 2 ha due flussi, un flusso audio e un flusso video con codifica DV. Questo grafico usa il [filtro DV Muxer](dv-muxer-filter.md) per combinare i flussi audio e video. Invia il flusso interleaved al filtro MSDV, ma suddivide nuovamente il flusso per l'anteprima.

Compilare questo grafico come indicato di seguito:


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

I primi due connettono il filtro di origine alla barra di divisione AVI e alla barra di divisione AVI al DV Mux. Nella prima chiamata, Capture Graph Builder aggiunge automaticamente lo splitter AVI al grafo e connette uno dei pin di output di AVI Splitter al DV Mux. Nella seconda chiamata, Capture Graph Builder trova il secondo pin di output dello splitter AVI e lo connette al DV Mux.

La terza chiamata **a RenderStream** connette il DV Muxer al filtro Infinite Pin Tee. La chiamata successiva connette un flusso dal tee pin infinito al filtro di acquisizione MSDV. Questo flusso viene trasmesso al dispositivo. L'ultima chiamata **a RenderStream** compila la sezione di anteprima del grafico.

Se non si vuole visualizzare l'anteprima durante la trasmissione, è possibile omettere infinite pin tee e semplicemente connettere il DV Mux al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



