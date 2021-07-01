---
description: Controllo di un grafo di acquisizione
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controllo di un grafo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00573256c1c010e23dfc598ceca5ac62d772711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119476"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="92b48-103">Controllo di un grafo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="92b48-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="92b48-104">L'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) di Filter Graph Manager include metodi per l'esecuzione, l'arresto e la sospensione dell'intero grafico.</span><span class="sxs-lookup"><span data-stu-id="92b48-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="92b48-105">Se il grafico dei filtri include flussi di acquisizione e anteprima, tuttavia, è probabile che si voglia controllare i due flussi in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="92b48-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="92b48-106">Ad esempio, è possibile visualizzare in anteprima il video senza acquisirlo.</span><span class="sxs-lookup"><span data-stu-id="92b48-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="92b48-107">È possibile eseguire questa operazione tramite [**il metodo ICaptureGraphBuilder2::ControlStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream)</span><span class="sxs-lookup"><span data-stu-id="92b48-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="92b48-108">Questo metodo non funziona durante l'acquisizione in un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="92b48-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="92b48-109">Controllo del flusso di acquisizione</span><span class="sxs-lookup"><span data-stu-id="92b48-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="92b48-110">Il codice seguente imposta l'esecuzione del flusso di acquisizione video per quattro secondi, a partire da un secondo dopo l'esecuzione del grafo:</span><span class="sxs-lookup"><span data-stu-id="92b48-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


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



<span data-ttu-id="92b48-111">Il primo parametro specifica il flusso da controllare, come GUID di categoria pin.</span><span class="sxs-lookup"><span data-stu-id="92b48-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="92b48-112">Il secondo parametro fornisce il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="92b48-112">The second parameter gives the media type.</span></span> <span data-ttu-id="92b48-113">Il terzo parametro è un puntatore al filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="92b48-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="92b48-114">Per controllare tutti i flussi di acquisizione nel grafico, impostare il secondo e il terzo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="92b48-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="92b48-115">I due parametri successivi definiscono gli orari di avvio e arresto del flusso, in relazione all'ora di inizio dell'esecuzione del grafico.</span><span class="sxs-lookup"><span data-stu-id="92b48-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="92b48-116">Chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="92b48-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="92b48-117">Fino a quando non si esegue il grafico, **il metodo ControlStream** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="92b48-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="92b48-118">Se il grafico è già in esecuzione, le impostazioni vengono applicate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="92b48-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="92b48-119">Gli ultimi due parametri vengono usati per ottenere le notifiche degli eventi all'avvio e all'arresto del flusso.</span><span class="sxs-lookup"><span data-stu-id="92b48-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="92b48-120">Per ogni flusso che si controlla usando questo metodo, il grafico dei filtri invia una coppia di eventi: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) all'avvio del flusso e [**EC STREAM CONTROL \_ \_ \_ STOPPED**](ec-stream-control-stopped.md) all'arresto del flusso.</span><span class="sxs-lookup"><span data-stu-id="92b48-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="92b48-121">I valori **di wStartCookie e** **wStopCookie** vengono usati come secondo parametro dell'evento.</span><span class="sxs-lookup"><span data-stu-id="92b48-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="92b48-122">Pertanto, *lParam2 nell'evento* di avvio è uguale **a wStartCookie** e *lParam2* nell'evento di arresto è uguale **a wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="92b48-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="92b48-123">Il codice seguente illustra come ottenere questi eventi:</span><span class="sxs-lookup"><span data-stu-id="92b48-123">The following code shows how to get these events:</span></span>


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



<span data-ttu-id="92b48-124">Il **metodo ControlStream** definisce alcuni valori speciali per l'ora di inizio e di arresto.</span><span class="sxs-lookup"><span data-stu-id="92b48-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="92b48-125">Valore</span><span class="sxs-lookup"><span data-stu-id="92b48-125">Value</span></span> | <span data-ttu-id="92b48-126">Inizia</span><span class="sxs-lookup"><span data-stu-id="92b48-126">Start</span></span>                                  | <span data-ttu-id="92b48-127">Stop</span><span class="sxs-lookup"><span data-stu-id="92b48-127">Stop</span></span>                               |
|-------------|----------------------------------------|---------|
| <span data-ttu-id="92b48-128">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="92b48-128">MAXLONGLONG</span></span> | <span data-ttu-id="92b48-129">Non avviare mai questo flusso.</span><span class="sxs-lookup"><span data-stu-id="92b48-129">Never start this stream.</span></span>               | <span data-ttu-id="92b48-130">Non arrestarsi finché il grafico non si arresta.</span><span class="sxs-lookup"><span data-stu-id="92b48-130">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="92b48-131">**NULL**</span><span class="sxs-lookup"><span data-stu-id="92b48-131">**NULL**</span></span>    | <span data-ttu-id="92b48-132">Iniziare immediatamente quando viene eseguito il grafo.</span><span class="sxs-lookup"><span data-stu-id="92b48-132">Start immediately when the graph runs.</span></span> | <span data-ttu-id="92b48-133">Arrestarsi immediatamente.</span><span class="sxs-lookup"><span data-stu-id="92b48-133">Stop immediately.</span></span>                  |



 

<span data-ttu-id="92b48-134">Ad esempio, il codice seguente arresta immediatamente il flusso di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="92b48-134">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="92b48-135">Anche se è possibile arrestare il flusso di acquisizione e riavviarlo in un secondo momento, verrà creato un gap nei timestamp.</span><span class="sxs-lookup"><span data-stu-id="92b48-135">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="92b48-136">Durante la riproduzione, il video apparirà bloccato durante il gap (a seconda del formato di file).</span><span class="sxs-lookup"><span data-stu-id="92b48-136">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="92b48-137">Controllo del flusso di anteprima</span><span class="sxs-lookup"><span data-stu-id="92b48-137">Controlling the Preview Stream</span></span>

<span data-ttu-id="92b48-138">Per controllare il pin di anteprima, chiamare **ControlStream** ma impostare il primo parametro su PIN \_ CATEGORY \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="92b48-138">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="92b48-139">Funziona esattamente come per PIN CATEGORY CAPTURE, ad eccezione del fatto che non è possibile usare le ore di riferimento per specificare l'inizio e l'arresto, perché i fotogrammi di anteprima non hanno \_ \_ timestamp.</span><span class="sxs-lookup"><span data-stu-id="92b48-139">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="92b48-140">Pertanto, è necessario utilizzare **NULL** o MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="92b48-140">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="92b48-141">Usare **NULL per** avviare il flusso di anteprima:</span><span class="sxs-lookup"><span data-stu-id="92b48-141">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="92b48-142">Usare MAXLONGLONG per arrestare il flusso di anteprima:</span><span class="sxs-lookup"><span data-stu-id="92b48-142">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="92b48-143">Non è importante se il flusso di anteprima proviene da un pin di anteprima nel filtro di acquisizione o dal filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="92b48-143">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="92b48-144">Il **metodo ControlStream** funziona in entrambi i modi.</span><span class="sxs-lookup"><span data-stu-id="92b48-144">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="92b48-145">Per i pin della porta video, tuttavia, il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="92b48-145">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="92b48-146">In tal caso, un altro approccio consiste nel nascondere la finestra video.</span><span class="sxs-lookup"><span data-stu-id="92b48-146">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="92b48-147">Eseguire una query sul grafico **per IVideoWindow** e usare il metodo [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) per visualizzare o nascondere la finestra.</span><span class="sxs-lookup"><span data-stu-id="92b48-147">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


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



<span data-ttu-id="92b48-148">Inoltre, se chiami [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore OAFALSE prima di eseguire il grafico, il filtro Renderer video nasconde la finestra fino a quando non si specifica diversamente.</span><span class="sxs-lookup"><span data-stu-id="92b48-148">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="92b48-149">Per impostazione predefinita, il renderer video mostra la finestra quando si esegue il grafo.</span><span class="sxs-lookup"><span data-stu-id="92b48-149">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="92b48-150">Osservazioni sul controllo stream</span><span class="sxs-lookup"><span data-stu-id="92b48-150">Remarks about Stream Control</span></span>

<span data-ttu-id="92b48-151">Il comportamento predefinito di un segnaposto è la consegna di campioni durante l'esecuzione del grafo.</span><span class="sxs-lookup"><span data-stu-id="92b48-151">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="92b48-152">Si supponga, ad esempio, di chiamare **ControlStream** con PIN \_ CATEGORY CAPTURE ma non con PIN CATEGORY \_ \_ \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="92b48-152">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="92b48-153">Quando si esegue il grafico, il flusso di anteprima verrà eseguito immediatamente, mentre il flusso di acquisizione verrà eseguito in qualsiasi momento specificato in **ControlStream.**</span><span class="sxs-lookup"><span data-stu-id="92b48-153">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="92b48-154">Se si acquisisce più di un flusso e li si invia a un filtro mux, ad esempio se si acquisisce audio e video in un file AVI, è necessario controllare entrambi i flussi in tandem.</span><span class="sxs-lookup"><span data-stu-id="92b48-154">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="92b48-155">In caso contrario, il filtro mux potrebbe bloccarsi in attesa di un flusso, mentre tenta di interfoliare i due flussi.</span><span class="sxs-lookup"><span data-stu-id="92b48-155">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="92b48-156">Impostare le stesse ore di avvio e arresto in tutti i flussi di acquisizione prima di eseguire il grafico:</span><span class="sxs-lookup"><span data-stu-id="92b48-156">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="92b48-157">Internamente, il metodo **ControlStream** usa l'interfaccia [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) che viene esposta sui pin del filtro di acquisizione, il filtro Smart Tee (se presente) ed eventualmente il filtro mux.</span><span class="sxs-lookup"><span data-stu-id="92b48-157">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="92b48-158">È possibile usare questa interfaccia direttamente, invece di chiamare **ControlStream**, anche se non c'è un particolare vantaggio a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="92b48-158">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92b48-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92b48-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b48-160">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="92b48-160">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



