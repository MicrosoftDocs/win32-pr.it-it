---
description: Controllo di un grafico di acquisizione
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controllo di un grafico di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522033"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="0f64c-103">Controllo di un grafico di acquisizione</span><span class="sxs-lookup"><span data-stu-id="0f64c-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="0f64c-104">L'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) del gestore del grafo del filtro dispone di metodi per l'esecuzione, l'arresto e la sospensione dell'intero grafico.</span><span class="sxs-lookup"><span data-stu-id="0f64c-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="0f64c-105">Se il grafo del filtro contiene flussi di acquisizione e di anteprima, è possibile, tuttavia, controllare i due flussi in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="0f64c-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="0f64c-106">Ad esempio, potrebbe essere necessario visualizzare l'anteprima del video senza acquisirlo.</span><span class="sxs-lookup"><span data-stu-id="0f64c-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="0f64c-107">Questa operazione può essere eseguita tramite il metodo [**ICaptureGraphBuilder2:: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .</span><span class="sxs-lookup"><span data-stu-id="0f64c-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="0f64c-108">Questo metodo non funziona durante l'acquisizione in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="0f64c-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="0f64c-109">Controllo del flusso di acquisizione</span><span class="sxs-lookup"><span data-stu-id="0f64c-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="0f64c-110">Il codice seguente imposta il flusso di acquisizione video da eseguire per quattro secondi, a partire da un secondo dopo l'esecuzione del grafo:</span><span class="sxs-lookup"><span data-stu-id="0f64c-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="0f64c-111">Il primo parametro specifica il flusso da controllare come GUID di categoria pin.</span><span class="sxs-lookup"><span data-stu-id="0f64c-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="0f64c-112">Il secondo parametro fornisce il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0f64c-112">The second parameter gives the media type.</span></span> <span data-ttu-id="0f64c-113">Il terzo parametro è un puntatore al filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0f64c-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="0f64c-114">Per controllare tutti i flussi di acquisizione nel grafico, impostare il secondo e il terzo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="0f64c-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="0f64c-115">I due parametri successivi definiscono i tempi di avvio e arresto del flusso, rispetto all'ora di inizio dell'esecuzione del grafico.</span><span class="sxs-lookup"><span data-stu-id="0f64c-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="0f64c-116">Chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="0f64c-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="0f64c-117">Fino a quando non si esegue il grafo, il metodo **ControlStream** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0f64c-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="0f64c-118">Se il grafo è già in esecuzione, le impostazioni diventano effettive immediatamente.</span><span class="sxs-lookup"><span data-stu-id="0f64c-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="0f64c-119">Gli ultimi due parametri vengono usati per ricevere notifiche degli eventi quando il flusso viene avviato e interrotto.</span><span class="sxs-lookup"><span data-stu-id="0f64c-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="0f64c-120">Per ogni flusso controllato usando questo metodo, il grafico dei filtri invia una coppia di eventi: il [**controllo del flusso EC viene \_ \_ \_ avviato**](ec-stream-control-started.md) all'avvio del flusso e il controllo del flusso di EC si interrompe quando il flusso viene [**\_ \_ \_ arrestato**](ec-stream-control-stopped.md) .</span><span class="sxs-lookup"><span data-stu-id="0f64c-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="0f64c-121">I valori di **wStartCookie** e **wStopCookie** vengono usati come secondo parametro dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0f64c-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="0f64c-122">Quindi, *lParam2* nell'evento di avvio è uguale a **wStartCookie** e *lParam2* nell'evento Stop è uguale a **wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="0f64c-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="0f64c-123">Il codice seguente mostra come ottenere questi eventi:</span><span class="sxs-lookup"><span data-stu-id="0f64c-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="0f64c-124">Il metodo **ControlStream** definisce alcuni valori speciali per le ore di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="0f64c-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="0f64c-125">Inizia</span><span class="sxs-lookup"><span data-stu-id="0f64c-125">Start</span></span>                                  | <span data-ttu-id="0f64c-126">Stop</span><span class="sxs-lookup"><span data-stu-id="0f64c-126">Stop</span></span>                               |
| <span data-ttu-id="0f64c-127">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="0f64c-127">MAXLONGLONG</span></span> | <span data-ttu-id="0f64c-128">Non avviare mai questo flusso.</span><span class="sxs-lookup"><span data-stu-id="0f64c-128">Never start this stream.</span></span>               | <span data-ttu-id="0f64c-129">Non arrestare finché il grafico non viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="0f64c-129">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="0f64c-130">**NULL**</span><span class="sxs-lookup"><span data-stu-id="0f64c-130">**NULL**</span></span>    | <span data-ttu-id="0f64c-131">Inizia immediatamente quando il grafico viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f64c-131">Start immediately when the graph runs.</span></span> | <span data-ttu-id="0f64c-132">Arresta immediatamente.</span><span class="sxs-lookup"><span data-stu-id="0f64c-132">Stop immediately.</span></span>                  |



 

<span data-ttu-id="0f64c-133">Ad esempio, il codice seguente arresta immediatamente il flusso di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="0f64c-133">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="0f64c-134">Sebbene sia possibile arrestare il flusso di acquisizione e riavviarlo in un secondo momento, verrà creato un gap nei timestamp.</span><span class="sxs-lookup"><span data-stu-id="0f64c-134">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="0f64c-135">Durante la riproduzione, il video verrà bloccato durante il gap (a seconda del formato di file).</span><span class="sxs-lookup"><span data-stu-id="0f64c-135">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="0f64c-136">Controllo del flusso di anteprima</span><span class="sxs-lookup"><span data-stu-id="0f64c-136">Controlling the Preview Stream</span></span>

<span data-ttu-id="0f64c-137">Per controllare il pin di anteprima, chiamare **ControlStream** ma impostare il primo parametro su \_ Aggiungi \_ anteprima categoria.</span><span class="sxs-lookup"><span data-stu-id="0f64c-137">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="0f64c-138">Questa operazione funziona esattamente come per l' \_ acquisizione di categorie pin \_ , ma non è possibile usare i tempi di riferimento per specificare l'avvio e l'arresto, perché i frame di anteprima non hanno timestamp.</span><span class="sxs-lookup"><span data-stu-id="0f64c-138">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="0f64c-139">Pertanto, è necessario utilizzare **null** o MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="0f64c-139">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="0f64c-140">Usare **null** per avviare il flusso di anteprima:</span><span class="sxs-lookup"><span data-stu-id="0f64c-140">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="0f64c-141">Usare MAXLONGLONG per arrestare il flusso di anteprima:</span><span class="sxs-lookup"><span data-stu-id="0f64c-141">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="0f64c-142">Non è importante se il flusso di anteprima deriva da un pin di anteprima nel filtro di acquisizione o dal filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="0f64c-142">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="0f64c-143">Il metodo **ControlStream** funziona in qualsiasi modo.</span><span class="sxs-lookup"><span data-stu-id="0f64c-143">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="0f64c-144">Per i pin della porta video, tuttavia, il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0f64c-144">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="0f64c-145">In tal caso, un altro approccio consiste nel nascondere la finestra video.</span><span class="sxs-lookup"><span data-stu-id="0f64c-145">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="0f64c-146">Eseguire una query sul grafo per **IVideoWindow** e usare il metodo [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) per mostrare o nascondere la finestra.</span><span class="sxs-lookup"><span data-stu-id="0f64c-146">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="0f64c-147">Inoltre, se si chiama [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore OAFALSE prima di eseguire il grafo, il filtro renderer video nasconde la finestra fino a quando non viene specificato diversamente.</span><span class="sxs-lookup"><span data-stu-id="0f64c-147">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="0f64c-148">Per impostazione predefinita, il renderer video mostra la finestra quando si esegue il grafo.</span><span class="sxs-lookup"><span data-stu-id="0f64c-148">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="0f64c-149">Osservazioni sul controllo Stream</span><span class="sxs-lookup"><span data-stu-id="0f64c-149">Remarks about Stream Control</span></span>

<span data-ttu-id="0f64c-150">Il comportamento predefinito per un PIN consiste nel recapitare gli esempi durante l'esecuzione del grafo.</span><span class="sxs-lookup"><span data-stu-id="0f64c-150">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="0f64c-151">Si supponga, ad esempio, di chiamare **ControlStream** con l' \_ acquisizione della categoria pin \_ , ma non con l' \_ anteprima della categoria pin \_ .</span><span class="sxs-lookup"><span data-stu-id="0f64c-151">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="0f64c-152">Quando si esegue il grafo, il flusso di anteprima viene eseguito immediatamente, mentre il flusso di acquisizione viene eseguito in qualsiasi momento specificato in **ControlStream**.</span><span class="sxs-lookup"><span data-stu-id="0f64c-152">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="0f64c-153">Se si acquisisce più di un flusso e lo si invia a un filtro Mux, ad esempio se si acquisisce audio e video in un file AVI, è necessario controllare entrambi i flussi in tandem.</span><span class="sxs-lookup"><span data-stu-id="0f64c-153">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="0f64c-154">In caso contrario, il filtro Mux potrebbe bloccarsi in attesa di un flusso, in quanto tenta di eseguire l'interleave dei due flussi.</span><span class="sxs-lookup"><span data-stu-id="0f64c-154">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="0f64c-155">Impostare le stesse ore di inizio e di fine su tutti i flussi di acquisizione prima di eseguire il grafo:</span><span class="sxs-lookup"><span data-stu-id="0f64c-155">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="0f64c-156">Internamente, il metodo **ControlStream** usa l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , esposta nei pin del filtro di acquisizione, il filtro di Smart Tee (se presente) e possibilmente il filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="0f64c-156">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="0f64c-157">È possibile utilizzare direttamente questa interfaccia, anziché chiamare **ControlStream**, anche se non esiste un particolare vantaggio.</span><span class="sxs-lookup"><span data-stu-id="0f64c-157">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f64c-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f64c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f64c-159">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0f64c-159">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



