---
description: Come riprodurre un file
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Come riprodurre un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401307"
---
# <a name="how-to-play-a-file"></a>Come riprodurre un file

Questo articolo ha lo scopo di offrire la versione di programmazione DirectShow. Presenta una semplice applicazione console che riproduce un file audio o video. Il programma è costituito solo da poche righe, ma illustra alcune potenzialità della programmazione DirectShow.

Come illustrato nell'articolo [Introduzione alla programmazione di applicazioni DirectShow](introduction-to-directshow-application-programming.md) , un'applicazione DirectShow esegue sempre gli stessi passaggi di base:

1.  Creare un'istanza del [gestore del grafo dei filtri](filter-graph-manager.md).
2.  Usare Filter Graph Manager per creare un grafico di filtro.
3.  Eseguire il grafo, causando il passaggio dei dati attraverso i filtri.

Per compilare e collegare il codice in questo argomento, includere il file di intestazione dshow. h e il collegamento al file di libreria statica strmiids. lib. Per altre informazioni, vedere [compilazione di applicazioni DirectShow](setting-up-the-build-environment.md).

Iniziare chiamando [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Per semplificare le operazioni, questo esempio ignora il valore restituito, ma è consigliabile controllare sempre il valore **HRESULT** da qualsiasi chiamata al metodo.

Chiamare quindi [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore del grafico del filtro:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Come illustrato, l'identificatore di classe (CLSID) è CLSID \_ filtergraph. Filter Graph Manager è fornito da una DLL in-process, quindi il contesto di esecuzione è **CLSCTX \_ InProc \_ server**. DirectShow supporta il modello di threading libero, quindi è anche possibile chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COinit \_ multithreading** .

La chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) restituisce l'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , che contiene la maggior parte dei metodi per la compilazione del grafico del filtro. Per questo esempio sono necessarie altre due interfacce:

-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controlla i flussi. Contiene i metodi per arrestare e avviare il grafo.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) dispone di metodi per ottenere gli eventi dal gestore del grafico dei filtri. In questo esempio l'interfaccia viene usata per attendere il completamento della riproduzione.

Entrambe le interfacce sono esposte dal gestore del grafico dei filtri. Usare il puntatore [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) restituito per eseguire una query:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



A questo punto è possibile compilare il grafico dei filtri. Per la riproduzione di file, questa operazione viene eseguita tramite una singola chiamata al metodo:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



Il metodo [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafico di filtro in grado di riprodurre il file specificato. Il primo parametro è il nome del file, rappresentato come stringa di caratteri wide (2 byte). Il secondo parametro è riservato e deve essere uguale a **null**.

Questo metodo può avere esito negativo se il file specificato non esiste o il formato di file non è riconosciuto. Supponendo che il metodo abbia esito positivo, tuttavia, il grafico a filtro è ora pronto per la riproduzione. Per eseguire il grafo, chiamare il metodo [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :


```C++
hr = pControl->Run();
```



Quando viene eseguito il grafico di filtro, i dati vengono spostati tra i filtri e vengono visualizzati come video e audio. La riproduzione avviene in un thread separato. È possibile attendere il completamento della riproduzione chiamando il metodo [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Questo metodo si blocca fino a quando non viene eseguita la riproduzione del file o fino a quando non scade l'intervallo di timeout specificato. Il valore infinito indica che l'applicazione viene bloccata per un tempo illimitato fino a quando non viene eseguita la riproduzione del file. Per un esempio più realistico di gestione degli eventi, vedere [rispondere agli eventi](responding-to-events.md).

Al termine dell'applicazione, rilasciare i puntatori all'interfaccia e chiudere la libreria COM:


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

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> </dl>

 

 
