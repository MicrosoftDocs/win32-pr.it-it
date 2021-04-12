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
# <a name="how-to-play-a-file"></a><span data-ttu-id="e7440-103">Come riprodurre un file</span><span class="sxs-lookup"><span data-stu-id="e7440-103">How To Play a File</span></span>

<span data-ttu-id="e7440-104">Questo articolo ha lo scopo di offrire la versione di programmazione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e7440-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="e7440-105">Presenta una semplice applicazione console che riproduce un file audio o video.</span><span class="sxs-lookup"><span data-stu-id="e7440-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="e7440-106">Il programma è costituito solo da poche righe, ma illustra alcune potenzialità della programmazione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e7440-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="e7440-107">Come illustrato nell'articolo [Introduzione alla programmazione di applicazioni DirectShow](introduction-to-directshow-application-programming.md) , un'applicazione DirectShow esegue sempre gli stessi passaggi di base:</span><span class="sxs-lookup"><span data-stu-id="e7440-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="e7440-108">Creare un'istanza del [gestore del grafo dei filtri](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="e7440-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="e7440-109">Usare Filter Graph Manager per creare un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="e7440-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="e7440-110">Eseguire il grafo, causando il passaggio dei dati attraverso i filtri.</span><span class="sxs-lookup"><span data-stu-id="e7440-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="e7440-111">Per compilare e collegare il codice in questo argomento, includere il file di intestazione dshow. h e il collegamento al file di libreria statica strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="e7440-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="e7440-112">Per altre informazioni, vedere [compilazione di applicazioni DirectShow](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e7440-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="e7440-113">Iniziare chiamando [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com:</span><span class="sxs-lookup"><span data-stu-id="e7440-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="e7440-114">Per semplificare le operazioni, questo esempio ignora il valore restituito, ma è consigliabile controllare sempre il valore **HRESULT** da qualsiasi chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="e7440-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="e7440-115">Chiamare quindi [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore del grafico del filtro:</span><span class="sxs-lookup"><span data-stu-id="e7440-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="e7440-116">Come illustrato, l'identificatore di classe (CLSID) è CLSID \_ filtergraph.</span><span class="sxs-lookup"><span data-stu-id="e7440-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="e7440-117">Filter Graph Manager è fornito da una DLL in-process, quindi il contesto di esecuzione è **CLSCTX \_ InProc \_ server**.</span><span class="sxs-lookup"><span data-stu-id="e7440-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="e7440-118">DirectShow supporta il modello di threading libero, quindi è anche possibile chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COinit \_ multithreading** .</span><span class="sxs-lookup"><span data-stu-id="e7440-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="e7440-119">La chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) restituisce l'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , che contiene la maggior parte dei metodi per la compilazione del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="e7440-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="e7440-120">Per questo esempio sono necessarie altre due interfacce:</span><span class="sxs-lookup"><span data-stu-id="e7440-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="e7440-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controlla i flussi.</span><span class="sxs-lookup"><span data-stu-id="e7440-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="e7440-122">Contiene i metodi per arrestare e avviare il grafo.</span><span class="sxs-lookup"><span data-stu-id="e7440-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="e7440-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) dispone di metodi per ottenere gli eventi dal gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="e7440-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="e7440-124">In questo esempio l'interfaccia viene usata per attendere il completamento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e7440-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="e7440-125">Entrambe le interfacce sono esposte dal gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="e7440-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="e7440-126">Usare il puntatore [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) restituito per eseguire una query:</span><span class="sxs-lookup"><span data-stu-id="e7440-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="e7440-127">A questo punto è possibile compilare il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="e7440-127">Now you can build the filter graph.</span></span> <span data-ttu-id="e7440-128">Per la riproduzione di file, questa operazione viene eseguita tramite una singola chiamata al metodo:</span><span class="sxs-lookup"><span data-stu-id="e7440-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="e7440-129">Il metodo [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafico di filtro in grado di riprodurre il file specificato.</span><span class="sxs-lookup"><span data-stu-id="e7440-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="e7440-130">Il primo parametro è il nome del file, rappresentato come stringa di caratteri wide (2 byte).</span><span class="sxs-lookup"><span data-stu-id="e7440-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="e7440-131">Il secondo parametro è riservato e deve essere uguale a **null**.</span><span class="sxs-lookup"><span data-stu-id="e7440-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="e7440-132">Questo metodo può avere esito negativo se il file specificato non esiste o il formato di file non è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e7440-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="e7440-133">Supponendo che il metodo abbia esito positivo, tuttavia, il grafico a filtro è ora pronto per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e7440-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="e7440-134">Per eseguire il grafo, chiamare il metodo [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :</span><span class="sxs-lookup"><span data-stu-id="e7440-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="e7440-135">Quando viene eseguito il grafico di filtro, i dati vengono spostati tra i filtri e vengono visualizzati come video e audio.</span><span class="sxs-lookup"><span data-stu-id="e7440-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="e7440-136">La riproduzione avviene in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="e7440-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="e7440-137">È possibile attendere il completamento della riproduzione chiamando il metodo [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :</span><span class="sxs-lookup"><span data-stu-id="e7440-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="e7440-138">Questo metodo si blocca fino a quando non viene eseguita la riproduzione del file o fino a quando non scade l'intervallo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="e7440-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="e7440-139">Il valore infinito indica che l'applicazione viene bloccata per un tempo illimitato fino a quando non viene eseguita la riproduzione del file.</span><span class="sxs-lookup"><span data-stu-id="e7440-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="e7440-140">Per un esempio più realistico di gestione degli eventi, vedere [rispondere agli eventi](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="e7440-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="e7440-141">Al termine dell'applicazione, rilasciare i puntatori all'interfaccia e chiudere la libreria COM:</span><span class="sxs-lookup"><span data-stu-id="e7440-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="e7440-142">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="e7440-142">Example Code</span></span>

<span data-ttu-id="e7440-143">Ecco il codice completo per l'esempio descritto in questo articolo:</span><span class="sxs-lookup"><span data-stu-id="e7440-143">Here is the complete code for the example described in this article:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e7440-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7440-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7440-145">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="e7440-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
