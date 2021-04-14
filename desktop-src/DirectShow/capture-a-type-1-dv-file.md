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
# <a name="capture-a-type-1-dv-file"></a>Acquisire un file DV di tipo 1

Un file AVI DV di tipo 1 contiene un singolo flusso con interfoliazione. Per acquisire un file di tipo 1 durante l'anteprima, utilizzare il grafico filtro illustrato nel diagramma seguente.

![acquisizione di tipo 1 con anteprima](images/dv1-cap.png)

I filtri in questo grafico includono:

-   Il filtro [Smart Tee](smart-tee-filter.md) suddivide il DV con interfoliazione in un flusso di acquisizione e in un flusso di anteprima. Entrambi i flussi contengono gli stessi dati con interfoliazione.
-   Il [Mux](avi-mux-filter.md) e il [writer di file](file-writer-filter.md) scrivono il flusso con interfoliazione su disco.
-   La [barra di divisione DV](dv-splitter-filter.md) suddivide il flusso con interfoliazione in un flusso video DV e un flusso audio. Entrambi i flussi vengono renderizzati per l'anteprima.
-   Il [decodificatore video DV](dv-video-decoder-filter.md) decodifica il flusso video DV per la visualizzazione in anteprima.

Compilare questo grafico come segue:


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



1.  Chiamare [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) per connettere il filtro Mux AVI al filtro del writer di file.
2.  Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con l'acquisizione della categoria pin della categoria pin \_ \_ per eseguire il rendering del flusso di acquisizione. Il generatore del grafico di acquisizione inserisce automaticamente il filtro di Smart Tee.
3.  Chiamare nuovamente RenderStream, ma con l'anteprima della categoria pin Category PIN \_ \_ , per eseguire il rendering del flusso di anteprima. Ignorare questa chiamata se non si desidera visualizzare in anteprima il video.

Per entrambe le chiamate a RenderStream, il tipo di supporto è MEDIATYPE con \_ interfoliazione, ovvero video DV con interfoliazione. In questo codice, il generatore di grafici di acquisizione aggiunge automaticamente tutti i filtri necessari, ad eccezione del filtro di acquisizione MSDV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



