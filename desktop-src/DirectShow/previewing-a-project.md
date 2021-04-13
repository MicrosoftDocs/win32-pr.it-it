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
# <a name="previewing-a-project"></a><span data-ttu-id="847df-103">Visualizzazione in anteprima di un progetto</span><span class="sxs-lookup"><span data-stu-id="847df-103">Previewing a Project</span></span>

<span data-ttu-id="847df-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="847df-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="847df-105">Per visualizzare in anteprima un progetto, chiamare prima **CoCreateInstance** per creare un'istanza del motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="847df-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="847df-106">L'identificatore di classe è CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="847df-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="847df-107">Chiamare quindi il metodo [**IRenderEngine:: SetTimelineObject**](irenderengine-settimelineobject.md) per specificare la sequenza temporale di cui si sta eseguendo il rendering.</span><span class="sxs-lookup"><span data-stu-id="847df-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="847df-108">La prima volta che si visualizza in anteprima la sequenza temporale, eseguire le chiamate seguenti nell'ordine elencato:</span><span class="sxs-lookup"><span data-stu-id="847df-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="847df-109">Chiamare [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md) per specificare la parte della sequenza temporale da visualizzare in anteprima.</span><span class="sxs-lookup"><span data-stu-id="847df-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="847df-110">Facoltativa</span><span class="sxs-lookup"><span data-stu-id="847df-110">(Optional)</span></span>
2.  <span data-ttu-id="847df-111">Chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo.</span><span class="sxs-lookup"><span data-stu-id="847df-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="847df-112">Chiamare [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="847df-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="847df-113">Questo metodo connette ogni pin di output a un renderer video o a un renderer audio, completando il grafico.</span><span class="sxs-lookup"><span data-stu-id="847df-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="847df-114">Nell'esempio di codice seguente vengono illustrati questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="847df-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="847df-115">A questo punto, eseguire il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="847df-115">Now run the filter graph.</span></span> <span data-ttu-id="847df-116">Chiamare innanzitutto il metodo [**IRenderEngine:: GetFilterGraph**](irenderengine-getfiltergraph.md) per recuperare un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="847df-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="847df-117">Eseguire quindi una query su Filter Graph Manager per l'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="847df-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="847df-118">Utilizzare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) di Filter Graph Manager per attendere il completamento dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="847df-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="847df-119">È anche possibile cercare il grafo usando l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) di Filter Graph Manager, esattamente come si farebbe con un grafico di riproduzione di file.</span><span class="sxs-lookup"><span data-stu-id="847df-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="847df-120">Per visualizzare nuovamente l'anteprima del progetto, cercare di nuovo il grafico all'ora zero e chiamare di nuovo l' **esecuzione** .</span><span class="sxs-lookup"><span data-stu-id="847df-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="847df-121">Se si modifica il contenuto della sequenza temporale, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="847df-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="847df-122">Chiamare **SetRenderRange**.</span><span class="sxs-lookup"><span data-stu-id="847df-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="847df-123">Facoltativa</span><span class="sxs-lookup"><span data-stu-id="847df-123">(Optional)</span></span>
2.  <span data-ttu-id="847df-124">Chiamare **ConnectFrontEnd**.</span><span class="sxs-lookup"><span data-stu-id="847df-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="847df-125">Se il metodo **ConnectFrontEnd** restituisce un \_ avviso \_ OUTPUTRESET, chiamare **RenderOutputPins**.</span><span class="sxs-lookup"><span data-stu-id="847df-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="847df-126">(Se **ConnectFrontEnd** restituisce S \_ OK, è possibile ignorare questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="847df-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="847df-127">Ritentare il grafico fino all'ora zero.</span><span class="sxs-lookup"><span data-stu-id="847df-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="847df-128">Eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="847df-128">Run the graph.</span></span>

<span data-ttu-id="847df-129">Nell'esempio seguente vengono illustrati i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="847df-129">The following example shows these steps:</span></span>


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



<span data-ttu-id="847df-130">Per un esempio completo in cui viene caricato e visualizzato in anteprima un file di progetto, vedere [caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="847df-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="847df-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="847df-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847df-132">Gestione dei progetti di modifica video</span><span class="sxs-lookup"><span data-stu-id="847df-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="847df-133">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="847df-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



