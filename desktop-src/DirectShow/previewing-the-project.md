---
description: Anteprima del Project
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Anteprima del Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d17d5fd0c87d98db2dac0a7ace97a72e2107eeb252561bbc535a5bd8b4a56d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748261"
---
# <a name="previewing-the-project"></a>Anteprima del Project

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Per visualizzare in anteprima il progetto, è necessario un componente denominato motore di rendering *,* che compila un grafico DirectShow filtro da una sequenza temporale. Il grafico dei filtri è ciò che esegue effettivamente il rendering del progetto. È possibile usare il motore di rendering per visualizzare in anteprima un progetto o scrivere il file di output finale.

Questo articolo non illustra in dettaglio il motore di rendering. Per l'anteprima, sono necessarie solo alcune chiamate al metodo. È possibile trovare una discussione più approfondita, inclusa la modalità di scrittura dei file di output, in [Rendering di un Project](rendering-a-project.md). L'esempio di codice seguente illustra come costruire un grafo di anteprima.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Creare il motore di rendering usando la **funzione CoCreateInstance.** Chiamare quindi i metodi seguenti sull'interfaccia [**IRenderEngine del**](irenderengine.md) motore di rendering:

-   [**SetTimelineObject**](irenderengine-settimelineobject.md). Specifica la sequenza temporale da utilizzare.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Crea un grafico di filtro parziale, con un segnaposto di output per ogni gruppo nella sequenza temporale.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Completa il grafico di anteprima connettendo ogni pin di output a un renderer video o audio.

Dopo aver compilato il grafo, è possibile visualizzare in anteprima il progetto eseguendo il grafo, come si farebbe con qualsiasi DirectShow di filtro. Per prima cosa, ottenere un puntatore al grafico dei filtri chiamando il [**metodo IRenderEngine::GetFilterGraph.**](irenderengine-getfiltergraph.md)


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Eseguire una query sul grafico dei filtri [**per le interfacce IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**e IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent) Usare queste due interfacce per eseguire il grafico e attendere il completamento della riproduzione. Per una spiegazione dell'uso di queste interfacce, vedere [How To Play a File](how-to-play-a-file.md) and Responding to [Events](responding-to-events.md). Il codice seguente illustra un modo per usare queste interfacce.


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



Il codice in questo esempio blocca l'esecuzione del programma fino al completamento della riproduzione, a causa del parametro INFINITE nella chiamata al metodo [**IMediaEvent::WaitForCompletion.**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) Se si verificano problemi durante la riproduzione, tuttavia, il programma potrebbe smettere di rispondere. In un'applicazione reale usare un ciclo di messaggi per attendere il completamento della riproduzione. È anche consigliabile fornire all'utente un modo per interrompere la riproduzione.

Dopo aver terminato di usare il motore di rendering, chiamare sempre il [**metodo IRenderEngine::ScrapIt.**](irenderengine-scrapit.md) Questo metodo elimina il grafico dei filtri e rilascia tutte le risorse utilizzate dal motore di rendering.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caricamento e anteprima di un Project](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



