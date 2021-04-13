---
description: Visualizzazione in anteprima di un progetto
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Visualizzazione in anteprima di un progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341731"
---
# <a name="previewing-a-project"></a>Visualizzazione in anteprima di un progetto

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Per visualizzare in anteprima un progetto, chiamare prima **CoCreateInstance** per creare un'istanza del motore di rendering di base. L'identificatore di classe è CLSID \_ RenderEngine. Chiamare quindi il metodo [**IRenderEngine:: SetTimelineObject**](irenderengine-settimelineobject.md) per specificare la sequenza temporale di cui si sta eseguendo il rendering.

La prima volta che si visualizza in anteprima la sequenza temporale, eseguire le chiamate seguenti nell'ordine elencato:

1.  Chiamare [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md) per specificare la parte della sequenza temporale da visualizzare in anteprima. Facoltativa
2.  Chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo.
3.  Chiamare [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md). Questo metodo connette ogni pin di output a un renderer video o a un renderer audio, completando il grafico.

Nell'esempio di codice seguente vengono illustrati questi passaggi:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



A questo punto, eseguire il grafico del filtro. Chiamare innanzitutto il metodo [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) per recuperare un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gestore del grafico dei filtri. Eseguire quindi una query su Filter Graph Manager per l'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), come illustrato nel codice seguente:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Utilizzare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) di Filter Graph Manager per attendere il completamento dell'anteprima. È anche possibile cercare il grafo usando l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) di Filter Graph Manager, esattamente come si farebbe con un grafico di riproduzione di file.

Per visualizzare nuovamente l'anteprima del progetto, cercare di nuovo il grafico all'ora zero e chiamare di nuovo l' **esecuzione** . Se si modifica il contenuto della sequenza temporale, procedere come segue:

1.  Chiamare **SetRenderRange**. Facoltativa
2.  Chiamare **ConnectFrontEnd**.
3.  Se il metodo **ConnectFrontEnd** restituisce un \_ avviso \_ OUTPUTRESET, chiamare **RenderOutputPins**. (Se **ConnectFrontEnd** restituisce S \_ OK, è possibile ignorare questo passaggio.
4.  Ritentare il grafico fino all'ora zero.
5.  Eseguire il grafo.

Nell'esempio seguente vengono illustrati i passaggi seguenti:


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



Per un esempio completo in cui viene caricato e visualizzato in anteprima un file di progetto, vedere [caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei progetti di modifica video](managing-video-editing-projects.md)
</dt> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> </dl>

 

 



