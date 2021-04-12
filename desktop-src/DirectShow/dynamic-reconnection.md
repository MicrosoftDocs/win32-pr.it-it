---
description: Riconnessione dinamica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Riconnessione dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481852"
---
# <a name="dynamic-reconnection"></a><span data-ttu-id="63698-103">Riconnessione dinamica</span><span class="sxs-lookup"><span data-stu-id="63698-103">Dynamic Reconnection</span></span>

<span data-ttu-id="63698-104">Nella maggior parte dei filtri DirectShow non è possibile riconnettere i pin mentre il grafo esegue attivamente lo streaming dei dati.</span><span class="sxs-lookup"><span data-stu-id="63698-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="63698-105">Prima di riconnettere i pin, l'applicazione deve arrestare il grafo.</span><span class="sxs-lookup"><span data-stu-id="63698-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="63698-106">Tuttavia, alcuni filtri supportano la riconnessione del PIN durante l'esecuzione del grafo, un processo noto come riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="63698-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="63698-107">Questa operazione può essere eseguita dall'applicazione o da un filtro nel grafico.</span><span class="sxs-lookup"><span data-stu-id="63698-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="63698-108">Si consideri, ad esempio, il grafico nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="63698-108">As an example, consider the graph in the following illustration.</span></span>

![diagramma di compilazione dinamica del grafico](images/dyngraph.png)

<span data-ttu-id="63698-110">Uno scenario per la riconnessione dinamica potrebbe essere quello di rimuovere il filtro 2 dal grafico, mentre il grafo è in esecuzione e sostituirlo con un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="63698-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="63698-111">Per il funzionamento di questo scenario, è necessario che siano soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="63698-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="63698-112">Il pin di input sul filtro 3 (pin D) deve supportare l'interfaccia [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="63698-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="63698-113">Questa interfaccia consente la riconnessione del pin senza arrestare il filtro.</span><span class="sxs-lookup"><span data-stu-id="63698-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="63698-114">Il pin di output sul filtro 1 (pin A) deve essere in grado di bloccare il flusso dei dati multimediali mentre si verifica la riconnessione.</span><span class="sxs-lookup"><span data-stu-id="63698-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="63698-115">Nessun dato può spostarsi tra il pin A e il pin D durante la riconnessione.</span><span class="sxs-lookup"><span data-stu-id="63698-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="63698-116">In genere, ciò significa che il pin di output deve supportare l'interfaccia [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) .</span><span class="sxs-lookup"><span data-stu-id="63698-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="63698-117">Tuttavia, se il filtro 1 è il filtro che avvia la riconnessione, potrebbe disporre di un meccanismo interno per bloccare il proprio flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="63698-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="63698-118">La riconnessione dinamica prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="63698-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="63698-119">Blocca il flusso di dati dal pin A.</span><span class="sxs-lookup"><span data-stu-id="63698-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="63698-120">Riconnettere il pin a al pin D, possibilmente tramite un nuovo filtro intermedio.</span><span class="sxs-lookup"><span data-stu-id="63698-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="63698-121">Sbloccare il pin A in modo che i dati ricomincino a fluire nuovamente.</span><span class="sxs-lookup"><span data-stu-id="63698-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="63698-122">**Passaggio 1. Blocca il flusso di dati**</span><span class="sxs-lookup"><span data-stu-id="63698-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="63698-123">Per bloccare il flusso di dati, chiamare [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sul pin a. Questo metodo può essere chiamato in modo asincrono o sincrono.</span><span class="sxs-lookup"><span data-stu-id="63698-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="63698-124">Per chiamare il metodo in *modo asincrono*, creare un oggetto evento Win32 e passare l'handle di evento al metodo **Block** .</span><span class="sxs-lookup"><span data-stu-id="63698-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="63698-125">Il metodo restituirà immediatamente.</span><span class="sxs-lookup"><span data-stu-id="63698-125">The method will return immediately.</span></span> <span data-ttu-id="63698-126">Attendere che l'evento venga segnalato, usando una funzione come **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="63698-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="63698-127">Il pin segnala l'evento quando il flusso di dati è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="63698-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="63698-128">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="63698-128">For example:</span></span>


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



<span data-ttu-id="63698-129">Per chiamare il metodo in modo *sincrono*, è sufficiente passare il valore **null** anziché l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="63698-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="63698-130">A questo punto il metodo si bloccherà fino al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="63698-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="63698-131">Questo problema può verificarsi solo se il PIN è pronto per fornire un nuovo esempio.</span><span class="sxs-lookup"><span data-stu-id="63698-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="63698-132">Se il filtro è sospeso, l'operazione può richiedere un periodo di tempo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="63698-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="63698-133">Non eseguire pertanto la chiamata sincrona dal thread dell'applicazione principale.</span><span class="sxs-lookup"><span data-stu-id="63698-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="63698-134">Usare un thread di lavoro oppure chiamare il metodo in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="63698-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="63698-135">**Passaggio 2. Riconnettere i pin**</span><span class="sxs-lookup"><span data-stu-id="63698-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="63698-136">Per riconnettere i pin, eseguire una query su Filter Graph Manager per l'interfaccia **IGraphConfig** e chiamare [**IGraphConfig:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) o [**IGraphConfig:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span><span class="sxs-lookup"><span data-stu-id="63698-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="63698-137">Il metodo di **riconnessione** è più semplice da usare. esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="63698-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="63698-138">Arresta i filtri intermedi (filtro 2 nell'esempio) e li rimuove dal grafico.</span><span class="sxs-lookup"><span data-stu-id="63698-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="63698-139">Aggiunge nuovi filtri intermedi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="63698-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="63698-140">Connette tutti i pin.</span><span class="sxs-lookup"><span data-stu-id="63698-140">Connects all the pins.</span></span>
-   <span data-ttu-id="63698-141">Sospende o esegue i nuovi filtri per trovare la corrispondenza con lo stato del grafico.</span><span class="sxs-lookup"><span data-stu-id="63698-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="63698-142">Il metodo **Reconnect** include diversi parametri facoltativi che possono essere usati per specificare il tipo di supporto per la connessione pin e il filtro intermedio da usare.</span><span class="sxs-lookup"><span data-stu-id="63698-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="63698-143">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="63698-143">For example:</span></span>


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



<span data-ttu-id="63698-144">Per informazioni dettagliate, vedere la pagina di riferimento.</span><span class="sxs-lookup"><span data-stu-id="63698-144">For details, consult the reference page.</span></span> <span data-ttu-id="63698-145">Se il metodo di **riconnessione** non è sufficientemente flessibile, è possibile usare il metodo **RECONFIGURE** , che chiama un metodo di callback definito dall'applicazione per riconnettere i pin.</span><span class="sxs-lookup"><span data-stu-id="63698-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="63698-146">Per usare questo metodo, implementare l'interfaccia [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63698-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="63698-147">Prima di chiamare **RECONFIGURE**, bloccare il flusso di dati dal pin di output, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="63698-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="63698-148">Eseguire quindi il push di tutti i dati ancora in sospeso nella sezione del grafico che si sta riconnettendo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="63698-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="63698-149">Chiamare [**IPinConnection:: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) sul pin di input più a valle nella catena di riconnessione (pin D nell'esempio).</span><span class="sxs-lookup"><span data-stu-id="63698-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="63698-150">Passare un handle a un evento Win32.</span><span class="sxs-lookup"><span data-stu-id="63698-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="63698-151">Chiamare [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input che è immediatamente a valle dal pin di output in cui è stato bloccato il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="63698-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="63698-152">(In questo esempio, il flusso di dati è stato bloccato al pin A, quindi è necessario chiamare **EndOfStream** sul pin B).</span><span class="sxs-lookup"><span data-stu-id="63698-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="63698-153">Attendere che l'evento venga segnalato.</span><span class="sxs-lookup"><span data-stu-id="63698-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="63698-154">Il pin di input (pin D) segnala l'evento quando riceve la notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="63698-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="63698-155">Ciò indica che nessun dato è in viaggio tra i pin e che il chiamante può riconnettere i pin in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="63698-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="63698-156">Si noti che il metodo **IGraphConfig:: Reconnect** gestisce automaticamente i passaggi precedenti.</span><span class="sxs-lookup"><span data-stu-id="63698-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="63698-157">È necessario eseguire questi passaggi solo se si usa il metodo **RECONFIGURE** .</span><span class="sxs-lookup"><span data-stu-id="63698-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="63698-158">Dopo aver eseguito il push dei dati attraverso il grafo, chiamare **RECONFIGURE** e passare un puntatore all'interfaccia di callback **IGraphConfigCallback** .</span><span class="sxs-lookup"><span data-stu-id="63698-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="63698-159">Il gestore del grafo del filtro chiamerà il metodo [**IGraphConfigCallback:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) fornito.</span><span class="sxs-lookup"><span data-stu-id="63698-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="63698-160">**Passaggio 3. Sbloccare il flusso di dati**</span><span class="sxs-lookup"><span data-stu-id="63698-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="63698-161">Dopo aver riconnesso i pin, sbloccare il flusso di dati chiamando **IPinFlowControl:: Block** con un valore pari a zero per il primo parametro.</span><span class="sxs-lookup"><span data-stu-id="63698-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="63698-162">Se una riconnessione dinamica viene eseguita da un filtro, è necessario tenere presenti alcuni problemi di Threading.</span><span class="sxs-lookup"><span data-stu-id="63698-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="63698-163">Se il gestore del grafico del filtro tenta di arrestare il filtro, è possibile che si verifichi un deadlock, perché il grafico attende l'arresto del filtro, mentre al tempo stesso il filtro potrebbe essere in attesa del push dei dati nel grafico.</span><span class="sxs-lookup"><span data-stu-id="63698-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="63698-164">Per evitare il possibile deadlock, alcuni dei metodi descritti in questa sezione accettano un handle per un evento Win32.</span><span class="sxs-lookup"><span data-stu-id="63698-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="63698-165">Il filtro deve segnalare l'evento se il gestore del grafico del filtro tenta di arrestare il filtro.</span><span class="sxs-lookup"><span data-stu-id="63698-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="63698-166">Per ulteriori informazioni, vedere [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span><span class="sxs-lookup"><span data-stu-id="63698-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="63698-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63698-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63698-168">Creazione di grafici dinamici</span><span class="sxs-lookup"><span data-stu-id="63698-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



