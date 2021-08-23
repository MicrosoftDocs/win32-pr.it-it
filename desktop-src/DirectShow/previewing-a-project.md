---
description: Anteprima di un Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Anteprima di un Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159303c175c459b4d5d93ba4c7b4b2622caddac2a35d3474a3059ac703d62645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583560"
---
# <a name="previewing-a-project"></a>Anteprima di un Project

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Per visualizzare in anteprima un progetto, chiamare **prima CoCreateInstance** per creare un'istanza del motore di rendering di base. L'identificatore di classe è CLSID \_ RenderEngine. Chiamare quindi il [**metodo IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) per specificare la sequenza temporale di cui si esegue il rendering.

La prima volta che si visualizza in anteprima la sequenza temporale, eseguire le chiamate seguenti nell'ordine elencato:

1.  Chiamare [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) per specificare quale parte della sequenza temporale visualizzare in anteprima. Facoltativa
2.  Chiamare [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo.
3.  Chiamare [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md). Questo metodo connette ogni segnaposto di output a un renderer video o a un renderer audio, completando il grafico.

L'esempio di codice seguente illustra questi passaggi:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Eseguire ora il grafico dei filtri. Chiamare prima il [**metodo IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) per recuperare un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) di Filter Graph Manager. Eseguire quindi una query su Filter Graph Manager per [**l'interfaccia IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), come illustrato nel codice seguente:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Usare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) di Filter Graph Manager per attendere il completamento dell'anteprima. È anche possibile cercare il grafo usando l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) di Filter Graph Manager, esattamente come si farebbe con un grafico di riproduzione di file.

Per visualizzare nuovamente in anteprima il progetto, tornare al tempo zero per il grafo e chiamare **di nuovo Esegui.** Se si modifica il contenuto della sequenza temporale, eseguire le operazioni seguenti:

1.  Chiamare **SetRenderRange**. Facoltativa
2.  Chiamare **ConnectFrontEnd**.
3.  Se il **metodo ConnectFrontEnd** restituisce S \_ WARN \_ OUTPUTRESET, chiamare **RenderOutputPins**. (Se **ConnectFrontEnd** restituisce S \_ È possibile ignorare questo passaggio.
4.  Cercare il grafo indietro al tempo zero.
5.  Eseguire il grafo.

L'esempio seguente illustra questi passaggi:


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



Per un esempio completo che carica e visualizza in anteprima un file di progetto, vedere Caricamento e anteprima di [un Project](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei progetti di modifica video](managing-video-editing-projects.md)
</dt> <dt>

[Rendering di un Project](rendering-a-project.md)
</dt> </dl>

 

 



