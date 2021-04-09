---
description: Visualizzazione in anteprima del progetto
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Visualizzazione in anteprima del progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965771"
---
# <a name="previewing-the-project"></a>Visualizzazione in anteprima del progetto

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Per visualizzare in anteprima il progetto, è necessario un componente denominato *motore di rendering*, che compila un grafico di filtro DirectShow da una sequenza temporale. Il grafico del filtro è quello che esegue effettivamente il rendering del progetto. È possibile utilizzare il motore di rendering per visualizzare un'anteprima di un progetto o per scrivere il file di output finale.

In questo articolo non vengono illustrati in dettaglio il motore di rendering. Per l'anteprima sono necessarie solo alcune chiamate al metodo. È possibile trovare una discussione più approfondita, inclusa la modalità di scrittura dei file di output, durante [il rendering di un progetto](rendering-a-project.md). Nell'esempio di codice seguente viene illustrato come creare un grafico di anteprima.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Creare il motore di rendering utilizzando la funzione **CoCreateInstance** . Chiamare quindi i metodi seguenti sull'interfaccia [**IRenderEngine**](irenderengine.md) del motore di rendering:

-   [**SetTimelineObject**](irenderengine-settimelineobject.md). Specifica la sequenza temporale da utilizzare.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Compila un grafico di filtro parziale, con un pin di output per ogni gruppo nella sequenza temporale.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Completa il grafico di anteprima connettendo ogni pin di output a un renderer video o audio.

Una volta compilato il grafo, è possibile visualizzare in anteprima il progetto eseguendo il grafo, come si farebbe con qualsiasi grafico filtro DirectShow. Per prima cosa, ottenere un puntatore al grafico di filtro chiamando il metodo [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) .


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Eseguire una query sul grafico di filtro per le interfacce [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) . Usare queste due interfacce per eseguire il grafico e attendere il completamento della riproduzione. Per una spiegazione su come usare queste interfacce, vedere [come riprodurre un file](how-to-play-a-file.md) e [rispondere agli eventi](responding-to-events.md). Nel codice seguente viene illustrato un modo per utilizzare tali interfacce.


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



Il codice in questo esempio blocca l'esecuzione del programma fino al completamento della riproduzione, a causa del parametro infinito nella chiamata al metodo [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) . Se si verificano problemi durante la riproduzione, tuttavia, il programma potrebbe smettere di rispondere. In un'applicazione reale, utilizzare un ciclo di messaggi per attendere il completamento della riproduzione. È inoltre consigliabile fornire all'utente un modo per interrompere la riproduzione.

Al termine dell'utilizzo del motore di rendering, chiamare sempre il metodo [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) . Questo metodo elimina il grafo del filtro e rilascia tutte le risorse contenute nel motore di rendering.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



