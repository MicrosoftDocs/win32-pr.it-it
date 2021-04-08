---
description: Creazione di un grafico di filtro VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Creazione di un grafico di filtro VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876794"
---
# <a name="building-a-vmr-9-filter-graph"></a>Creazione di un grafico di filtro VMR-9

Poiché il filtro per la combinazione video di renderer 9 (VMR-9) non è il renderer video predefinito, un'applicazione che usa VMR-9 deve aggiungerla in modo esplicito al grafo e connetterla. Questa sezione presenta due approcci diversi per la creazione di grafici di filtro con VMR-9.

Uso del generatore di grafici di acquisizione

Il generatore di grafici di acquisizione è un oggetto helper per la creazione di grafici di filtri personalizzati. È possibile usarlo per compilare grafici VMR-9 come indicato di seguito:

1.  Creare e inizializzare il generatore di grafici di acquisizione, come descritto nell'argomento [relativo al generatore del grafico di acquisizione](about-the-capture-graph-builder.md).
2.  Chiamare CoCreateInstance per creare VMR-9:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) in Filter Graph Manager per aggiungere VMR-9 al grafico dei filtri:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Chiamare [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere un filtro di origine per il file video:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Chiamare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per eseguire il rendering del flusso video in VMR:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Facoltativamente, chiamare di nuovo RenderStream per eseguire il rendering del flusso audio:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

È possibile combinare diversi flussi video chiamando AddSourceFilter e RenderStream per ogni file di origine.

Utilizzo di Filter Graph Manager

Se si preferisce non usare il generatore Graph di acquisizione, è possibile compilare un grafo VMR-9 usando semplicemente i metodi in gestione grafico dei filtri, come indicato di seguito:

1.  Creare VMR-9 e aggiungerlo al grafo, come illustrato nella procedura precedente.
2.  Usare AddSourceFilter per aggiungere un filtro di origine per il file video, come illustrato nella procedura precedente.
3.  Se si desidera eseguire il rendering dell'audio, creare un'istanza del filtro di [renderer DirectSound](directsound-renderer-filter.md) e aggiungerla al grafico dei filtri.
4.  Usare il metodo IBaseFilter:: EnumPins per trovare un pin di output nel filtro di origine. Per informazioni dettagliate, vedere [enumerazione dei pin](enumerating-pins.md) .
5.  Eseguire una query su Filter Graph Manager per l'interfaccia IFilterGraph2.
6.  Chiamare [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) con il \_ flag AM RenderEx \_ RENDERTOEXISTINGRENDERERS. Questa chiamata esegue il rendering del PIN di output, usando solo i filtri renderer già presenti nel grafico, in questo caso VMR-9 e il renderer DirectSound. In questo modo si impedisce alla logica di connessione intelligente di aggiungere il renderer video predefinito al grafo, che lascerebbe VMR-9 non connesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di grafici con il generatore di grafici di acquisizione](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



