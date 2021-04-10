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
# <a name="transmit-from-type-1-file"></a>Trasmissione da un file di tipo 1

Per trasmettere un file di tipo 1 durante l'anteprima del file, usare il grafico di filtro illustrato nel diagramma seguente.

![tipo-1 trasmesso con anteprima](images/dv1-transmit.png)

I filtri in questo grafico includono:

-   Il [separatore AVI](avi-splitter-filter.md) analizza il file AVI. Per un file DV di tipo 1, il pin di output fornisce esempi DV con interfoliazione.
-   Il filtro del [Pin Tee infinito](infinite-pin-tee-filter.md) suddivide il DV con interfoliazione in un flusso di trasmissione e un flusso di anteprima. Entrambi i flussi contengono gli stessi dati con interfoliazione. (Questo grafico usa il Pin Tee infinito anziché il [Tee intelligente](smart-tee-filter.md), perché non vi è alcun rischio di eliminare i frame durante la lettura da un file, come avviene con l'acquisizione in tempo reale).
-   La [barra di divisione DV](dv-splitter-filter.md) suddivide il flusso con interfoliazione in un flusso video DV, decodificato dal [decodificatore video DV](dv-video-decoder-filter.md)e da un flusso audio. Entrambi i flussi vengono renderizzati per l'anteprima.

Compilare questo grafico come segue:


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



1.  Chiamare [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere il filtro di origine al grafico dei filtri.
2.  Creare il separatore AVI e l'infinito Pin Tee e aggiungerli al grafico.
3.  Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di origine al separatore AVI. Specificare MEDIATYPE \_ con interfoliazione per assicurarsi che il metodo non riesca se il file di origine non è un file DV di tipo 1. In tal caso, è possibile eseguire il backup e tentare di compilare invece un grafo di trasmissione di tipo 2.
4.  Chiamare di nuovo **RenderStream** per instradare il flusso con interfoliazione dal separatore AVI al tee infinito del PIN
5.  Chiamare RenderStream una terza volta per indirizzare un flusso dal tee infinito al filtro MSDV per la trasmissione al dispositivo.
6.  Chiamare **RenderStream** un'ultima volta per compilare la sezione di anteprima del grafo.

Se non si desidera visualizzare l'anteprima, connettere semplicemente l'origine file al filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



