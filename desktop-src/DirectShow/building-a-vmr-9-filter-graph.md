---
description: Compilazione di un filtro VMR-9 Graph
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Compilazione di un filtro VMR-9 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86a76b2d4519299bbd9cde498ccf6a4bc33f0b819d3996faac794154d08c8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689351"
---
# <a name="building-a-vmr-9-filter-graph"></a>Compilazione di un filtro VMR-9 Graph

Poiché il filtro del renderer video mixer 9 (VMR-9) non è il renderer video predefinito, un'applicazione che usa VMR-9 deve aggiungerlo in modo esplicito al grafo e connetterlo. In questa sezione vengono presentati due approcci diversi alla creazione di grafi di filtro con VMR-9.

Uso di Capture Graph Builder

Capture Graph Builder è un oggetto helper per la creazione di grafici filtro personalizzati. È possibile usarlo per creare grafici VMR-9 come indicato di seguito:

1.  Creare e inizializzare capture Graph Builder, come descritto nell'argomento [About the Capture Graph Builder](about-the-capture-graph-builder.md).
2.  Chiamare CoCreateInstance per creare vmr-9:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Chiamare [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) in Filter Graph Manager per aggiungere vmr-9 al grafico dei filtri:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Chiamare [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere un filtro di origine per il file video:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Chiamare il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per eseguire il rendering del flusso video nella macchina virtuale:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Facoltativamente, chiamare di nuovo RenderStream per eseguire il rendering del flusso audio:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

È possibile combinare diversi flussi video chiamando AddSourceFilter e RenderStream per ogni file di origine.

Uso di Filter Graph Manager

Se si preferisce non usare Capture Graph Builder, è possibile compilare un grafo VMR-9 semplicemente usando i metodi in Filter Graph Manager, come indicato di seguito:

1.  Creare la VMR-9 e aggiungerla al grafo, come illustrato nella procedura precedente.
2.  Usare AddSourceFilter per aggiungere un filtro di origine per il file video, come illustrato nella procedura precedente.
3.  Se si vuole eseguire il rendering dell'audio, creare un'istanza del filtro [DirectSound Renderer](directsound-renderer-filter.md) e aggiungerlo al grafico dei filtri.
4.  Usare il metodo IBaseFilter::EnumPins per trovare un pin di output nel filtro di origine. Per [informazioni dettagliate, vedere Enumerazione dei](enumerating-pins.md) pin.
5.  Eseguire una query su Filter Graph Manager per l'interfaccia IFilterGraph2.
6.  Chiamare [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) con il flag AM \_ RENDEREX \_ RENDERTOEXISTINGRENDERERS. Questa chiamata esegue il rendering del pin di output usando solo i filtri del renderer già presenti nel grafo, in questo caso VMR-9 e DirectSound Renderer. Ciò impedisce alla logica di Connessione intelligente di aggiungere il renderer video predefinito al grafo, in modo da lasciare la VMR-9 scollegata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di grafici con Capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



