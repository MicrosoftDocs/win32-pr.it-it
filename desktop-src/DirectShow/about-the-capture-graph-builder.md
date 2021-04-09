---
description: Informazioni sul generatore di grafici di acquisizione
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Informazioni sul generatore di grafici di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965795"
---
# <a name="about-the-capture-graph-builder"></a>Informazioni sul generatore di grafici di acquisizione

Un grafico di filtro che esegue l'acquisizione video o audio è denominato *grafico di acquisizione*. I grafici di acquisizione sono spesso più complicati dei grafici per la riproduzione di file. Per semplificare la creazione di grafici di acquisizione da parte delle applicazioni, DirectShow fornisce un oggetto helper denominato generatore grafico di acquisizione. Il generatore di grafici di acquisizione espone l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , che contiene i metodi per la compilazione e il controllo di un grafico di acquisizione. Il diagramma seguente illustra il generatore Graph di acquisizione e l'interfaccia **ICaptureGraphBuilder2** .

![uso del generatore di grafici di acquisizione](images/cgb01.png)

Per iniziare, chiamare CoCreateInstance per creare nuove istanze del generatore del grafico di acquisizione e del gestore del grafico dei filtri. Inizializzare quindi il generatore Graph di acquisizione chiamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gestore del grafico dei filtri. La figura seguente illustra questo processo.

![inizializzazione del generatore di grafici di acquisizione](images/cgb03.png)

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



In questa sezione sull'acquisizione video si presuppone che si stia usando il generatore del grafico di acquisizione per creare il grafico di acquisizione. Tuttavia, è possibile compilare i grafici di acquisizione interamente usando i metodi IGraphBuilder. Questo argomento è tuttavia considerato un argomento avanzato e i metodi di acquisizione del generatore di grafici sono preferiti. Per altre informazioni, vedere [argomenti di acquisizione avanzati](advanced-capture-topics.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su acquisizione video in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



