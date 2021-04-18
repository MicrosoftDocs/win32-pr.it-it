---
title: Modello asincrono
description: La maggior parte delle operazioni nell'API dei servizi Web Windows può essere eseguita in modo sincrono o asincrono.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Servizi Web del modello asincrono per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298358"
---
# <a name="asynchronous-model"></a><span data-ttu-id="31d83-106">Modello asincrono</span><span class="sxs-lookup"><span data-stu-id="31d83-106">Asynchronous Model</span></span>

<span data-ttu-id="31d83-107">La maggior parte delle operazioni nell'API dei servizi Web Windows può essere eseguita in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="31d83-108">Per chiamare una funzione in modo sincrono, passare un valore null per la struttura del [**\_ \_ contesto WS asincrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="31d83-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="31d83-109">Per specificare che una funzione può essere eseguita in modo asincrono, passare un **\_ \_ contesto WS asincrono** non null alla funzione.</span><span class="sxs-lookup"><span data-stu-id="31d83-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="31d83-110">Quando viene chiamato in modo asincrono, una funzione può comunque essere completata in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="31d83-111">Se la funzione viene completata in modo sincrono, restituisce un valore che indica l'esito positivo o negativo finale e questo valore è sempre diverso da **WS \_ S \_ Async** (vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="31d83-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="31d83-112">Un valore restituito di **WS \_ S \_ Async**, tuttavia, indica che la funzione viene completata in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="31d83-113">Quando la funzione viene completata in modo asincrono, viene richiamato un callback per segnalare il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="31d83-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="31d83-114">Questo callback indica il valore finale di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="31d83-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="31d83-115">Il callback non viene chiamato se l'operazione viene completata in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="31d83-116">Per creare un contesto asincrono, inizializzare i campi **callback** e **callbackState** della struttura del [**\_ \_ contesto WS asincrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="31d83-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="31d83-117">Il campo **callbackState** viene usato per specificare un puntatore ai dati definiti dall'utente che vengono passati alla funzione [**di \_ \_ callback WS asincrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="31d83-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="31d83-118">Nell'esempio seguente viene illustrata la chiamata di una funzione in modo asincrono passando un puntatore a una struttura del [**\_ \_ contesto WS asincrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) che contiene il callback e un puntatore ai dati di stato.</span><span class="sxs-lookup"><span data-stu-id="31d83-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

<span data-ttu-id="31d83-119">La struttura del [**\_ \_ contesto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asincrona viene utilizzata dalla funzione asincrona solo per la durata della chiamata di funzione (non per la durata dell'operazione asincrona), pertanto è possibile dichiararla in modo sicuro nello stack.</span><span class="sxs-lookup"><span data-stu-id="31d83-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="31d83-120">Se qualsiasi altro parametro, oltre alla struttura del [**\_ \_ contesto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asincrono, viene passato a una funzione asincrona come puntatori e la funzione viene completata in modo asincrono, è responsabilità del chiamante preservare i valori a cui puntano i parametri attivi (non liberati) fino a quando non viene richiamato il callback asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="31d83-121">Esistono limitazioni sulle operazioni che possono essere eseguite da un callback.</span><span class="sxs-lookup"><span data-stu-id="31d83-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="31d83-122">Per ulteriori informazioni sulle possibili operazioni, vedere il [**\_ \_ modello di callback WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span><span class="sxs-lookup"><span data-stu-id="31d83-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="31d83-123">Quando si implementa una funzione asincrona, non richiamare il callback sullo stesso thread che ha chiamato la funzione asincrona prima che la funzione asincrona venisse restituita al chiamante, in quanto questa operazione interrompe il modello asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="31d83-124">Quando si implementa una funzione che deve eseguire una serie di operazioni asincrone, provare a usare la funzione di supporto [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .</span><span class="sxs-lookup"><span data-stu-id="31d83-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="31d83-125">Nell' [esempio di funzione asincrona](asyncmodelexample.md) viene illustrato come implementare e utilizzare funzioni che seguono il modello asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="31d83-126">L'avvio di un'operazione di i/o asincrona utilizza risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="31d83-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="31d83-127">Se vengono avviate un numero sufficiente di operazioni di i/o, il sistema può smettere di rispondere.</span><span class="sxs-lookup"><span data-stu-id="31d83-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="31d83-128">Per evitare questo problema, un'applicazione deve limitare il numero di operazioni asincrone che avvia.</span><span class="sxs-lookup"><span data-stu-id="31d83-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="31d83-129">Il modello asincrono utilizza gli elementi API seguenti.</span><span class="sxs-lookup"><span data-stu-id="31d83-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="31d83-130">Callback</span><span class="sxs-lookup"><span data-stu-id="31d83-130">Callback</span></span>                                         | <span data-ttu-id="31d83-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31d83-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31d83-132">**\_callback asincrono \_ WS**</span><span class="sxs-lookup"><span data-stu-id="31d83-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="31d83-133">Il parametro della funzione di callback utilizzato con il modello asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="31d83-134">**\_funzione ws Async \_**</span><span class="sxs-lookup"><span data-stu-id="31d83-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="31d83-135">Utilizzato con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) per specificare la funzione successiva da richiamare in una serie di operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="31d83-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="31d83-136">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="31d83-136">Enumeration</span></span>                                      | <span data-ttu-id="31d83-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31d83-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31d83-138">**\_modello di callback WS \_**</span><span class="sxs-lookup"><span data-stu-id="31d83-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="31d83-139">Specifica il comportamento di threading di un callback (ad esempio, [**un \_ \_ callback WS asincrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span><span class="sxs-lookup"><span data-stu-id="31d83-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="31d83-140">Funzione</span><span class="sxs-lookup"><span data-stu-id="31d83-140">Function</span></span>                                 | <span data-ttu-id="31d83-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31d83-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31d83-142">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="31d83-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="31d83-143">Richiama un callback definito dall'utente che può avviare un'operazione asincrona e indicare una funzione che deve essere chiamata quando l'operazione asincrona è stata completata.</span><span class="sxs-lookup"><span data-stu-id="31d83-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="31d83-144">Struttura</span><span class="sxs-lookup"><span data-stu-id="31d83-144">Structure</span></span>                                          | <span data-ttu-id="31d83-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31d83-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31d83-146">**\_contesto asincrono \_ WS**</span><span class="sxs-lookup"><span data-stu-id="31d83-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="31d83-147">Specifica il callback asincrono e un puntatore ai dati definiti dall'utente, che verranno passati al callback asincrono.</span><span class="sxs-lookup"><span data-stu-id="31d83-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="31d83-148">**\_operazione asincrona \_ WS**</span><span class="sxs-lookup"><span data-stu-id="31d83-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="31d83-149">Utilizzato con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) per specificare la funzione successiva da richiamare in una serie di operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="31d83-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="31d83-150">**\_stato asincrono \_ WS**</span><span class="sxs-lookup"><span data-stu-id="31d83-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="31d83-151">Usato da [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) per gestire lo stato di un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="31d83-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="31d83-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31d83-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31d83-153">Esempio di funzione asincrona</span><span class="sxs-lookup"><span data-stu-id="31d83-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="31d83-154">**\_callback asincrono \_ WS**</span><span class="sxs-lookup"><span data-stu-id="31d83-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="31d83-155">**\_contesto asincrono \_ WS**</span><span class="sxs-lookup"><span data-stu-id="31d83-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="31d83-156">**\_modello di callback WS \_**</span><span class="sxs-lookup"><span data-stu-id="31d83-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="31d83-157">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="31d83-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




