---
description: Come riprodurre un file
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Come riprodurre un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d20a021ec5053746c279598d08117c6b25a5fe6a52946fed56f19eda3cafe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401149"
---
# <a name="how-to-play-a-file"></a>Come riprodurre un file

Questo articolo ha lo scopo di offrire la versione di DirectShow programmazione. Presenta una semplice applicazione console che riproduce un file audio o video. Il programma è lungo solo poche righe, ma dimostra alcune delle funzionalità della DirectShow programmazione.

Come descritto [nell'articolo](introduction-to-directshow-application-programming.md) Introduzione DirectShow programmazione di applicazioni, un'applicazione DirectShow esegue sempre gli stessi passaggi di base:

1.  Creare un'istanza di [Filter Graph Manager](filter-graph-manager.md).
2.  Usare Filter Graph Manager per creare un grafico di filtro.
3.  Eseguire il grafico, causando lo spostamento dei dati tra i filtri.

Per compilare e collegare il codice in questo argomento, includere il file di intestazione Dshow.h e il collegamento al file di libreria statica strmiids.lib. Per altre informazioni, vedere [Building DirectShow Applications](setting-up-the-build-environment.md).

Per iniziare, chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria COM:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Per semplicità, questo esempio ignora il valore restituito, ma è necessario controllare sempre il valore **HRESULT** da qualsiasi chiamata al metodo.

Chiamare quindi [**CoCreateInstance per**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) creare la gestione Graph filtro:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Come illustrato, l'identificatore di classe (CLSID) è CLSID \_ FilterGraph. La gestione Graph filtro viene fornita da una DLL in-process, quindi il contesto di esecuzione è **CLSCTX \_ INPROC \_ SERVER.** DirectShow supporta il modello di threading free, quindi è anche possibile chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COINIT \_ MULTITHREADED.**

La chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) restituisce [**l'interfaccia IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) che contiene principalmente metodi per la compilazione del grafico dei filtri. Per questo esempio sono necessarie altre due interfacce:

-   [**IMediaControl controlla**](/windows/desktop/api/Control/nn-control-imediacontrol) lo streaming. Contiene metodi per arrestare e avviare il grafico.
-   [**IMediaEvent include**](/windows/desktop/api/Control/nn-control-imediaevent) metodi per ottenere eventi da Filter Graph Manager. In questo esempio l'interfaccia viene usata per attendere il completamento della riproduzione.

Entrambe queste interfacce vengono esposte da Filter Graph Manager. Usare il [**puntatore IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) restituito per eseguire una query:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



A questo punto è possibile compilare il grafico dei filtri. Per la riproduzione di file, questa operazione viene eseguita da una singola chiamata al metodo:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



Il [**metodo IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafico di filtro in grado di riprodurre il file specificato. Il primo parametro è il nome del file, rappresentato come stringa di caratteri wide (2 byte). Il secondo parametro è riservato e deve essere uguale a **NULL.**

Questo metodo può avere esito negativo se il file specificato non esiste o se il formato di file non è riconosciuto. Supponendo che il metodo abbia esito positivo, tuttavia, il grafico dei filtri è ora pronto per la riproduzione. Per eseguire il grafo, chiamare il [**metodo IMediaControl::Run:**](/windows/desktop/api/Control/nf-control-imediacontrol-run)


```C++
hr = pControl->Run();
```



Quando viene eseguito il grafo dei filtri, i dati vengono spostati tra i filtri e sottoposti a rendering come video e audio. La riproduzione avviene in un thread separato. È possibile attendere il completamento della riproduzione chiamando il [**metodo IMediaEvent::WaitForCompletion:**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion)


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Questo metodo si blocca fino al termine della riproduzione del file o fino alla scadenza dell'intervallo di timeout specificato. Il valore INFINITE indica che l'applicazione si blocca per un periodo illimitato fino al termine della riproduzione del file. Per un esempio più realistico di gestione degli eventi, vedere [Risposta agli eventi](responding-to-events.md).

Al termine dell'applicazione, rilasciare i puntatori a interfaccia e chiudere la libreria COM:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Codice di esempio

Ecco il codice completo per l'esempio descritto in questo articolo:


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di DirectShow di base](basic-directshow-tasks.md)
</dt> </dl>

 

 
