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
# <a name="previewing-the-project"></a><span data-ttu-id="4d20c-103">Visualizzazione in anteprima del progetto</span><span class="sxs-lookup"><span data-stu-id="4d20c-103">Previewing the Project</span></span>

<span data-ttu-id="4d20c-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4d20c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4d20c-105">Per visualizzare in anteprima il progetto, è necessario un componente denominato *motore di rendering*, che compila un grafico di filtro DirectShow da una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4d20c-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="4d20c-106">Il grafico del filtro è quello che esegue effettivamente il rendering del progetto.</span><span class="sxs-lookup"><span data-stu-id="4d20c-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="4d20c-107">È possibile utilizzare il motore di rendering per visualizzare un'anteprima di un progetto o per scrivere il file di output finale.</span><span class="sxs-lookup"><span data-stu-id="4d20c-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="4d20c-108">In questo articolo non vengono illustrati in dettaglio il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="4d20c-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="4d20c-109">Per l'anteprima sono necessarie solo alcune chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="4d20c-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="4d20c-110">È possibile trovare una discussione più approfondita, inclusa la modalità di scrittura dei file di output, durante [il rendering di un progetto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="4d20c-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="4d20c-111">Nell'esempio di codice seguente viene illustrato come creare un grafico di anteprima.</span><span class="sxs-lookup"><span data-stu-id="4d20c-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="4d20c-112">Creare il motore di rendering utilizzando la funzione **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="4d20c-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="4d20c-113">Chiamare quindi i metodi seguenti sull'interfaccia [**IRenderEngine**](irenderengine.md) del motore di rendering:</span><span class="sxs-lookup"><span data-stu-id="4d20c-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="4d20c-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span><span class="sxs-lookup"><span data-stu-id="4d20c-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="4d20c-115">Specifica la sequenza temporale da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4d20c-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="4d20c-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="4d20c-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="4d20c-117">Compila un grafico di filtro parziale, con un pin di output per ogni gruppo nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4d20c-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="4d20c-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="4d20c-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="4d20c-119">Completa il grafico di anteprima connettendo ogni pin di output a un renderer video o audio.</span><span class="sxs-lookup"><span data-stu-id="4d20c-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="4d20c-120">Una volta compilato il grafo, è possibile visualizzare in anteprima il progetto eseguendo il grafo, come si farebbe con qualsiasi grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4d20c-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="4d20c-121">Per prima cosa, ottenere un puntatore al grafico di filtro chiamando il metodo [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="4d20c-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="4d20c-122">Eseguire una query sul grafico di filtro per le interfacce [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="4d20c-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="4d20c-123">Usare queste due interfacce per eseguire il grafico e attendere il completamento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4d20c-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="4d20c-124">Per una spiegazione su come usare queste interfacce, vedere [come riprodurre un file](how-to-play-a-file.md) e [rispondere agli eventi](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="4d20c-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="4d20c-125">Nel codice seguente viene illustrato un modo per utilizzare tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="4d20c-125">The following code shows one way to use these interfaces.</span></span>


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



<span data-ttu-id="4d20c-126">Il codice in questo esempio blocca l'esecuzione del programma fino al completamento della riproduzione, a causa del parametro infinito nella chiamata al metodo [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) .</span><span class="sxs-lookup"><span data-stu-id="4d20c-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="4d20c-127">Se si verificano problemi durante la riproduzione, tuttavia, il programma potrebbe smettere di rispondere.</span><span class="sxs-lookup"><span data-stu-id="4d20c-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="4d20c-128">In un'applicazione reale, utilizzare un ciclo di messaggi per attendere il completamento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4d20c-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="4d20c-129">È inoltre consigliabile fornire all'utente un modo per interrompere la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4d20c-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="4d20c-130">Al termine dell'utilizzo del motore di rendering, chiamare sempre il metodo [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="4d20c-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="4d20c-131">Questo metodo elimina il grafo del filtro e rilascia tutte le risorse contenute nel motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="4d20c-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="4d20c-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d20c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d20c-133">Caricamento e visualizzazione in anteprima di un progetto</span><span class="sxs-lookup"><span data-stu-id="4d20c-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



