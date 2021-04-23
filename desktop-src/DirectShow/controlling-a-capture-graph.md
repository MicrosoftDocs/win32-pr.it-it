---
description: Controllo di un grafo di acquisizione
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controllo di un grafo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909049"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="2b9cd-103">Controllo di un grafo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="2b9cd-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="2b9cd-104">L'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) di Filter Graph Manager include metodi per l'esecuzione, l'arresto e la sospensione dell'intero grafico.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="2b9cd-105">Se tuttavia il grafico dei filtri include flussi di acquisizione e anteprima, è probabile che si voglia controllare i due flussi in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="2b9cd-106">Ad esempio, è possibile visualizzare in anteprima il video senza acquisirlo.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="2b9cd-107">È possibile eseguire questa operazione tramite il [**metodo ICaptureGraphBuilder2::ControlStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream)</span><span class="sxs-lookup"><span data-stu-id="2b9cd-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="2b9cd-108">Questo metodo non funziona durante l'acquisizione in un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2b9cd-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="2b9cd-109">Controllo del flusso di acquisizione</span><span class="sxs-lookup"><span data-stu-id="2b9cd-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="2b9cd-110">Il codice seguente imposta l'esecuzione del flusso di acquisizione video per quattro secondi, a partire da un secondo dopo l'esecuzione del grafo:</span><span class="sxs-lookup"><span data-stu-id="2b9cd-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


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



<span data-ttu-id="2b9cd-111">Il primo parametro specifica il flusso da controllare, come GUID di categoria pin.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="2b9cd-112">Il secondo parametro fornisce il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-112">The second parameter gives the media type.</span></span> <span data-ttu-id="2b9cd-113">Il terzo parametro è un puntatore al filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="2b9cd-114">Per controllare tutti i flussi di acquisizione nel grafico, impostare il secondo e il terzo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="2b9cd-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="2b9cd-115">I due parametri successivi definiscono gli orari di avvio e arresto del flusso, rispetto all'ora di inizio dell'esecuzione del grafico.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="2b9cd-116">Chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="2b9cd-117">Fino a quando non si esegue il grafico, il **metodo ControlStream** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="2b9cd-118">Se il grafico è già in esecuzione, le impostazioni vengono applicate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="2b9cd-119">Gli ultimi due parametri vengono usati per ottenere notifiche degli eventi all'avvio e all'arresto del flusso.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="2b9cd-120">Per ogni flusso che si controlla usando questo metodo, il grafo dei filtri invia una coppia di eventi: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) all'avvio del flusso e [**EC STREAM CONTROL \_ \_ \_ STOPPED**](ec-stream-control-stopped.md) all'arresto del flusso.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="2b9cd-121">I valori **di wStartCookie e** **wStopCookie** vengono usati come secondo parametro dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="2b9cd-122">Pertanto, *lParam2 nell'evento* di avvio è uguale **a wStartCookie** e *lParam2* nell'evento di arresto è uguale **a wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="2b9cd-123">Il codice seguente illustra come ottenere questi eventi:</span><span class="sxs-lookup"><span data-stu-id="2b9cd-123">The following code shows how to get these events:</span></span>


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



<span data-ttu-id="2b9cd-124">Il **metodo ControlStream** definisce alcuni valori speciali per l'ora di inizio e di arresto.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="2b9cd-125">Label</span><span class="sxs-lookup"><span data-stu-id="2b9cd-125">Label</span></span> | <span data-ttu-id="2b9cd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2b9cd-126">Value</span></span> |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="2b9cd-127">Inizia</span><span class="sxs-lookup"><span data-stu-id="2b9cd-127">Start</span></span>                                  | <span data-ttu-id="2b9cd-128">Stop</span><span class="sxs-lookup"><span data-stu-id="2b9cd-128">Stop</span></span>                               |
| <span data-ttu-id="2b9cd-129">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="2b9cd-129">MAXLONGLONG</span></span> | <span data-ttu-id="2b9cd-130">Non avviare mai questo flusso.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-130">Never start this stream.</span></span>               | <span data-ttu-id="2b9cd-131">Non arrestarsi fino a quando il grafico non si arresta.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-131">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="2b9cd-132">**NULL**</span><span class="sxs-lookup"><span data-stu-id="2b9cd-132">**NULL**</span></span>    | <span data-ttu-id="2b9cd-133">Iniziare immediatamente quando viene eseguito il grafo.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-133">Start immediately when the graph runs.</span></span> | <span data-ttu-id="2b9cd-134">Arrestarsi immediatamente.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-134">Stop immediately.</span></span>                  |



 

<span data-ttu-id="2b9cd-135">Ad esempio, il codice seguente arresta immediatamente il flusso di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="2b9cd-135">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="2b9cd-136">Anche se è possibile arrestare il flusso di acquisizione e riavviarlo in un secondo momento, verrà creato un gap nei timestamp.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-136">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="2b9cd-137">Durante la riproduzione, il video apparirà bloccato durante il gap (a seconda del formato di file).</span><span class="sxs-lookup"><span data-stu-id="2b9cd-137">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="2b9cd-138">Controllo del flusso di anteprima</span><span class="sxs-lookup"><span data-stu-id="2b9cd-138">Controlling the Preview Stream</span></span>

<span data-ttu-id="2b9cd-139">Per controllare il pin di anteprima, chiamare **ControlStream** ma impostare il primo parametro su PIN \_ CATEGORY \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-139">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="2b9cd-140">Questa operazione funziona esattamente come per PIN CATEGORY CAPTURE, ad eccezione del fatto che non è possibile usare le ore di riferimento per specificare l'inizio e l'arresto, perché i fotogrammi di anteprima non hanno \_ \_ timestamp.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-140">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="2b9cd-141">Pertanto, è necessario utilizzare **NULL** o MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-141">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="2b9cd-142">Usare **NULL per** avviare il flusso di anteprima:</span><span class="sxs-lookup"><span data-stu-id="2b9cd-142">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="2b9cd-143">Usare MAXLONGLONG per arrestare il flusso di anteprima:</span><span class="sxs-lookup"><span data-stu-id="2b9cd-143">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="2b9cd-144">Non è importante se il flusso di anteprima proviene da un pin di anteprima nel filtro di acquisizione o dal filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-144">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="2b9cd-145">Il **metodo ControlStream** funziona in entrambi i modi.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-145">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="2b9cd-146">Per i pin di porta video, tuttavia, il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-146">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="2b9cd-147">In tal caso, un altro approccio consiste nel nascondere la finestra video.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-147">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="2b9cd-148">Eseguire una query sul **grafo per IVideoWindow** e usare il metodo [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) per visualizzare o nascondere la finestra.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-148">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


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



<span data-ttu-id="2b9cd-149">Inoltre, se si chiama [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore OAFALSE prima di eseguire il grafico, il filtro renderer video nasconde la finestra fino a quando non si specifica diversamente.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-149">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="2b9cd-150">Per impostazione predefinita, il renderer video mostra la finestra quando si esegue il grafico.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-150">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="2b9cd-151">Osservazioni sul controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="2b9cd-151">Remarks about Stream Control</span></span>

<span data-ttu-id="2b9cd-152">Il comportamento predefinito per un segnaposto è fornire esempi quando viene eseguito il grafo.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-152">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="2b9cd-153">Si supponga, ad esempio, di chiamare **ControlStream** con PIN \_ CATEGORY CAPTURE ma non con PIN CATEGORY \_ \_ \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-153">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="2b9cd-154">Quando si esegue il grafico, il flusso di anteprima verrà eseguito immediatamente, mentre il flusso di acquisizione verrà eseguito in qualsiasi momento specificato in **ControlStream**.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-154">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="2b9cd-155">Se si acquisisce più di un flusso e li si invia a un filtro mux, ad esempio se si acquisisce audio e video in un file AVI, è necessario controllare entrambi i flussi in tandem.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-155">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="2b9cd-156">In caso contrario, il filtro mux potrebbe bloccarsi in attesa di un flusso, mentre tenta di interfoliare i due flussi.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-156">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="2b9cd-157">Impostare gli stessi orari di avvio e arresto in tutti i flussi di acquisizione prima di eseguire il grafico:</span><span class="sxs-lookup"><span data-stu-id="2b9cd-157">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="2b9cd-158">Internamente, il metodo **ControlStream** usa l'interfaccia [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) esposta sui pin del filtro di acquisizione, il filtro Smart Tee (se presente) ed eventualmente il filtro mux.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-158">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="2b9cd-159">È possibile usare questa interfaccia direttamente, invece di chiamare **ControlStream**, anche se non esiste alcun vantaggio particolare a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="2b9cd-159">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b9cd-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b9cd-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b9cd-161">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2b9cd-161">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



