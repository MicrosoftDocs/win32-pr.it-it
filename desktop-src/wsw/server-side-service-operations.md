---
title: Operazioni del servizio sul lato server
description: In questa sezione vengono descritte le operazioni del servizio sul lato servizio.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Servizi Web per le operazioni del servizio sul lato server per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399942"
---
# <a name="server-side-service-operations"></a><span data-ttu-id="bf272-106">Operazioni del servizio sul lato server</span><span class="sxs-lookup"><span data-stu-id="bf272-106">Server Side Service Operations</span></span>

<span data-ttu-id="bf272-107">In questa sezione vengono descritte le operazioni del servizio sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="bf272-107">This section describes service side service operations.</span></span>


<span data-ttu-id="bf272-108">Di seguito è riportato il layout di un'operazione del servizio sul lato server</span><span class="sxs-lookup"><span data-stu-id="bf272-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="bf272-109">contesto [del \_ \_ contesto dell'operazione](ws-operation-context.md) const WS \* : il [contesto](context.md)dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf272-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="bf272-110">Parametri delle operazioni di servizio: parametri relativi all'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="bf272-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="bf272-111">const [**WS \_ Async \_ context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contesto asincrono per eseguire le operazioni del servizio in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="bf272-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="bf272-112">[WS \_ Errore](ws-error.md) \* : oggetto Rich Error.</span><span class="sxs-lookup"><span data-stu-id="bf272-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a><span data-ttu-id="bf272-113">Gestione degli errori e degli errori</span><span class="sxs-lookup"><span data-stu-id="bf272-113">Fault And Error Handling</span></span>

<span data-ttu-id="bf272-114">Il lato server deve usare errori per recapitare le condizioni di errore al client.</span><span class="sxs-lookup"><span data-stu-id="bf272-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="bf272-115">Questa operazione può essere eseguita restituendo un HRESULT con esito negativo e incorporando l'errore nell'oggetto Error.</span><span class="sxs-lookup"><span data-stu-id="bf272-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="bf272-116">Se l'errore non è impostato sull'oggetto Error e viene restituito un errore HRESULT, l'infrastruttura tenterà di recapitare un errore al client.</span><span class="sxs-lookup"><span data-stu-id="bf272-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="bf272-117">Il livello dei dettagli divulgato al client in tal caso è controllato dalla proprietà del servizio [**di \_ \_ \_ \_ divulgazione degli errori della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) nell'host del [servizio](service-host.md).</span><span class="sxs-lookup"><span data-stu-id="bf272-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="bf272-118">Completamento chiamata</span><span class="sxs-lookup"><span data-stu-id="bf272-118">Call Completion</span></span>

<span data-ttu-id="bf272-119">Una chiamata a un'operazione di servizio lato server sincrona viene definita completa quando restituisce il controllo all'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="bf272-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="bf272-120">Per un'operazione asincrona del servizio, una chiamata viene considerata completa dopo che la notifica di callback viene rilasciata dall'implementazione dell'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="bf272-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="bf272-121">Durata chiamata</span><span class="sxs-lookup"><span data-stu-id="bf272-121">Call Lifetime</span></span>

<span data-ttu-id="bf272-122">È necessario prestare particolare attenzione quando si implementa un'operazione del servizio sul lato server per la sua durata.</span><span class="sxs-lookup"><span data-stu-id="bf272-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="bf272-123">La durata di una chiamata può influire significativamente sul tempo impiegato dall'host del servizio per l'arresto.</span><span class="sxs-lookup"><span data-stu-id="bf272-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="bf272-124">Se si prevede che un'operazione del servizio sul lato server si blocchi a causa di alcune operazioni di i/o associate, è consigliabile registrare un callback di annullamento in modo da ricevere una notifica in caso di interruzione dell'host del servizio o quando la connessione sottostante viene chiusa dal client.</span><span class="sxs-lookup"><span data-stu-id="bf272-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="bf272-125">Operazioni del servizio lato server e considerazione della memoria</span><span class="sxs-lookup"><span data-stu-id="bf272-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="bf272-126">Se un'operazione del servizio deve allocare memoria per i parametri in uscita, deve utilizzare l'oggetto dell' [ \_ heap WS](ws-heap.md) disponibile tramite il [ \_ \_ contesto dell'operazione WS](ws-operation-context.md).</span><span class="sxs-lookup"><span data-stu-id="bf272-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="bf272-127">Esempio: operazione del servizio e \_ heap WS</span><span class="sxs-lookup"><span data-stu-id="bf272-127">Example: Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a><span data-ttu-id="bf272-128">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="bf272-128">Return Values</span></span>

-   <span data-ttu-id="bf272-129">WS \_ S \_ Async: la chiamata verrà completata in Async.</span><span class="sxs-lookup"><span data-stu-id="bf272-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="bf272-130">WS \_ S \_ end: la chiamata è stata completata correttamente. il server non è in attesa di alcun [ \_ messaggio WS](ws-message.md) dal client oltre questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf272-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="bf272-131">Se \_ viene visualizzato un altro messaggio WS, il server deve interrompere il canale.</span><span class="sxs-lookup"><span data-stu-id="bf272-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="bf272-132">NOERROR/tutti gli altri HRESULT di esito positivo: la chiamata è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bf272-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="bf272-133">Si noti che è consigliabile che l'applicazione non restituisca HRESULT other quindi NOERROR per completare correttamente l'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="bf272-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="bf272-134">Tutto con un errore HRESULT: viene restituito un errore al client se ne è disponibile uno in WS \_ Error.</span><span class="sxs-lookup"><span data-stu-id="bf272-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="bf272-135">In caso contrario, un errore generico viene inviato di nuovo al client.</span><span class="sxs-lookup"><span data-stu-id="bf272-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="bf272-136">Vedere la discussione sull'errore sopra.</span><span class="sxs-lookup"><span data-stu-id="bf272-136">See fault discussion above.</span></span>

<span data-ttu-id="bf272-137">Vedere, [chiamare l'annullamento](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="bf272-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




