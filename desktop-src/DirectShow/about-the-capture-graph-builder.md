---
description: Informazioni su Capture Graph Builder
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Informazioni su Capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ef82a160ada6e53fe6d2db830efa85118eb699074630905cd41f0b5412ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664520"
---
# <a name="about-the-capture-graph-builder"></a>Informazioni su Capture Graph Builder

Un grafo di filtro che esegue l'acquisizione video o audio è detto *grafico di acquisizione.* I grafici di acquisizione sono spesso più complessi rispetto ai grafici di riproduzione dei file. Per semplificare la compilazione di grafici di acquisizione da parte delle applicazioni, DirectShow un oggetto helper denominato Capture Graph Builder. Capture Graph Builder espone [**l'interfaccia ICaptureGraphBuilder2,**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) che contiene i metodi per la compilazione e il controllo di un grafo di acquisizione. Il diagramma seguente illustra l'interfaccia Capture Graph Builder e **ICaptureGraphBuilder2.**

![uso del generatore di grafi di acquisizione](images/cgb01.png)

Per iniziare, chiamare CoCreateInstance per creare nuove istanze di Capture Graph Builder e filter Graph Manager. Inizializzare quindi Capture Graph Builder chiamando [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) di Filter Graph Manager. La figura seguente illustra questo processo.

![inizializzazione del generatore di grafi di acquisizione](images/cgb03.png)

Il codice seguente illustra una funzione helper per eseguire questi passaggi:


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



In questa sezione sull'acquisizione video si presuppone che si sta usando Capture Graph Builder per creare il grafico di acquisizione. Tuttavia, è possibile creare grafici di acquisizione interamente usando i metodi IGraphBuilder. Questo è considerato un argomento avanzato, tuttavia, e i metodi capture Graph Builder sono preferibili. Per altre informazioni, vedere [Argomenti di acquisizione avanzata](advanced-capture-topics.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'acquisizione video in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



