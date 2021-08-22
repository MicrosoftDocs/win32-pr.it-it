---
description: Trasmettere dal file di tipo 1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Trasmettere dal file di tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ce67627c350c24de1bf1ee96ba7804ac3f164264e167498c597e8136ea138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015534"
---
# <a name="transmit-from-type-1-file"></a>Trasmettere dal file di tipo 1

Per trasmettere un file di tipo 1 durante l'anteprima del file, usare il grafico dei filtri illustrato nel diagramma seguente.

![trasmissione di tipo 1 con anteprima](images/dv1-transmit.png)

I filtri in questo grafico includono:

-   Lo [splitter AVI analizza](avi-splitter-filter.md) il file AVI. Per un file DV di tipo 1, il pin di output fornisce esempi di DV interleaved.
-   Il [filtro Infinite Pin Tee](infinite-pin-tee-filter.md) suddivide la DV interleaved in un flusso di trasmissione e in un flusso di anteprima. Entrambi i flussi contengono gli stessi dati interleaved. Questo grafo usa il tee Infinite Pin invece di [Smart Tee,](smart-tee-filter.md)perché non esiste alcun rischio di eliminazione dei fotogrammi durante la lettura da un file, come nel caso dell'acquisizione live.
-   Lo [splitter DV](dv-splitter-filter.md) suddivide il flusso interleaved in un flusso video DV, decodificato dal decodificatore [video DV,](dv-video-decoder-filter.md)e in un flusso audio. Entrambi i flussi sono rendererd per l'anteprima.

Compilare questo grafico come indicato di seguito:


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



1.  Chiamare [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere il filtro di origine al grafico dei filtri.
2.  Creare il separatore AVI e il tee pin infinito e aggiungerli al grafo.
3.  Chiamare [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di origine alla barra di divisione AVI. Specifica di MEDIATYPE Interleaved per assicurarsi che il metodo non riesca se il file di origine non è un file DV di tipo \_ 1. In tal caso, è possibile eseguire il back-out e provare a compilare un grafico di trasmissione di tipo 2.
4.  Chiamare **di nuovo RenderStream** per instradare il flusso interleaved dalla barra di divisione AVI al tee pin infinito
5.  Chiamare RenderStream una terza volta per instradare un flusso dal tee pin infinito al filtro MSDV, per la trasmissione al dispositivo.
6.  Chiamare **RenderStream un'ultima** volta per compilare la sezione di anteprima del grafico.

Se non si vuole visualizzare l'anteprima, è sufficiente connettere l'origine file al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



