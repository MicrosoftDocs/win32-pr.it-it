---
title: Operazioni del servizio sul lato client
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 'Altre informazioni su: operazioni del servizio sul lato client'
keywords:
- Servizi Web per le operazioni del servizio sul lato client per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232454"
---
# <a name="client-side-service-operations"></a><span data-ttu-id="9a3f2-106">Operazioni del servizio sul lato client</span><span class="sxs-lookup"><span data-stu-id="9a3f2-106">Client-side Service Operations</span></span>

<span data-ttu-id="9a3f2-107">Di seguito è riportato il layout di un'operazione del servizio sul lato client:</span><span class="sxs-lookup"><span data-stu-id="9a3f2-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="9a3f2-108">[WS \_ \_Proxy del servizio](ws-service-proxy.md) \* serviceProxy: [proxy del servizio](service-proxy.md) per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="9a3f2-109">[WS \_ Heap heap](ws-heap.md) \* : heap obbligatorio utilizzato per la serializzazione e la deserializzazione del corpo del [ \_ messaggio WS](ws-message.md).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="9a3f2-110">Parametri delle operazioni di servizio: parametri relativi all'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="9a3f2-111">[**Chiamare le proprietà e il relativo conteggio**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): una matrice di proprietà della chiamata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="9a3f2-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) Property Count: numero di proprietà della chiamata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="9a3f2-113">[**WS \_ \_Contesto**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asincrono asyncContext: contesto asincrono per l'esecuzione della chiamata in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="9a3f2-114">[WS \_ Errore:](ws-error.md) oggetto Rich Error.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="9a3f2-115">Firma per le operazioni del servizio sul lato client</span><span class="sxs-lookup"><span data-stu-id="9a3f2-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="9a3f2-116">Considerazioni sulla memoria per le operazioni del servizio sul lato client</span><span class="sxs-lookup"><span data-stu-id="9a3f2-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="9a3f2-117">La chiamata all'operazione del servizio accetta un [ \_ heap WS](ws-heap.md) \* come parametro.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="9a3f2-118">Si tratta di un parametro obbligatorio utilizzato per la serializzazione/deserializzazione di corpi dei messaggi nei parametri.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="9a3f2-119">L'applicazione deve chiamare [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) se la chiamata ha avuto esito positivo o meno.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="9a3f2-120">Se la chiamata ha esito positivo e presenta parametri in uscita, l'applicazione deve chiamare **WsResetHeap** immediatamente dopo che è stata completata con i parametri in uscita.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="9a3f2-121">L'applicazione deve allocare memoria per i parametri in e out con [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="9a3f2-122">Potrebbe essere necessario riallocare il proxy del servizio in modo che i puntatori forniti vengano sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="9a3f2-123">Un tentativo di liberare tale memoria provocherà l'arresto anomalo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="9a3f2-124">Operazione del servizio lato client e \_ heap WS</span><span class="sxs-lookup"><span data-stu-id="9a3f2-124">Client-side Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a><span data-ttu-id="9a3f2-125">Parametro error</span><span class="sxs-lookup"><span data-stu-id="9a3f2-125">Error parameter</span></span>

<span data-ttu-id="9a3f2-126">L'applicazione deve sempre passare il parametro error a:</span><span class="sxs-lookup"><span data-stu-id="9a3f2-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="9a3f2-127">Ottenere informazioni dettagliate sugli errori se si verifica un errore durante la chiamata dell'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="9a3f2-128">Ottenere l'oggetto errore se il servizio restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="9a3f2-129">L'errore è contenuto nell'oggetto Error.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-129">The fault is contained in the error object.</span></span> <span data-ttu-id="9a3f2-130">In questo caso, il valore **HRESULT** restituito dall'operazione del servizio è **WS \_ E \_ endpoint \_ \_ received** (vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="9a3f2-131">Proprietà delle chiamate per le operazioni del servizio sul lato client</span><span class="sxs-lookup"><span data-stu-id="9a3f2-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="9a3f2-132">Le proprietà di chiamata consentono a un'applicazione di specificare impostazioni personalizzate per una determinata chiamata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="9a3f2-133">Attualmente, solo una proprietà di chiamata è disponibile con il modello di servizio, [**\_ \_ \_ \_ ID chiamata della proprietà WS Call**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a><span data-ttu-id="9a3f2-134">Abbandono di una chiamata</span><span class="sxs-lookup"><span data-stu-id="9a3f2-134">Abandoning a Call</span></span>

<span data-ttu-id="9a3f2-135">Spesso è preferibile abbandonare i risultati di una chiamata per restituire il controllo all'applicazione, in modo che il completamento effettivo della chiamata venga gestito dall'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="9a3f2-136">Il proxy del servizio fornisce questa funzionalità tramite [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="9a3f2-137">Si noti che il controllo per il chiamante non può essere restituito immediatamente, l'unica garanzia che il runtime del proxy del servizio fornisce è che non attende il completamento di un'operazione di I/O, prima di restituire il controllo al chiamante.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="9a3f2-138">Le chiamate su un'operazione del servizio lato client possono essere abbandonate tramite una chiamata a [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="9a3f2-139">Accetta un proxy del servizio e un ID chiamata. Un ID chiamata viene fornito come parte di una proprietà di chiamata in un'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="9a3f2-140">Se l'ID chiamata è 0, il proxy del servizio abbandonerà tutte le chiamate in sospeso a tale istanza.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="9a3f2-141">Timeout delle chiamate</span><span class="sxs-lookup"><span data-stu-id="9a3f2-141">Call Timeouts</span></span>

<span data-ttu-id="9a3f2-142">Per impostazione predefinita, un proxy del servizio ha un timeout di 30 secondi per ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="9a3f2-143">Il timeout di una chiamata può essere modificato dalla proprietà del proxy del servizio di [**timeout delle chiamate della \_ \_ Proprietà WS \_ \_ proxy**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) durante la creazione di un proxy del servizio tramite [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="9a3f2-144">Una volta raggiunto il timeout, la chiamata viene abbandonata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="9a3f2-145">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="9a3f2-145">Return Values</span></span>

<span data-ttu-id="9a3f2-146">Tutti i valori **HRESULT** di esito positivo devono essere considerati come esito positivo e tutti i valori di errore devono essere considerati come errori.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="9a3f2-147">Di seguito sono riportati alcuni dei valori **HRESULT** che un'applicazione può aspettarsi:</span><span class="sxs-lookup"><span data-stu-id="9a3f2-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="9a3f2-148">**WS \_ S \_ Async**: la chiamata verrà completata in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="9a3f2-149">NOERROR: la chiamata è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="9a3f2-150">**WS \_ \_Operazione E \_ abbandonata**: la chiamata è stata abbandonata.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="9a3f2-151">L'oggetto Error contiene il motivo dell'abbandono.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="9a3f2-152">**WS \_ \_ \_ Operazione non valida**: il proxy del servizio non si trova in uno stato appropriato per effettuare una chiamata, controllare lo stato del proxy del servizio per determinare lo stato del proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="9a3f2-153">Per un elenco completo dei valori restituiti, vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="9a3f2-154">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="9a3f2-154">Code Examples</span></span>

<span data-ttu-id="9a3f2-155">Per esempi di codice, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a3f2-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="9a3f2-156">CallAbandonExample</span><span class="sxs-lookup"><span data-stu-id="9a3f2-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="9a3f2-157">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="9a3f2-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




