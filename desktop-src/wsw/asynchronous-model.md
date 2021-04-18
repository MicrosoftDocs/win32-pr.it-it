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
# <a name="asynchronous-model"></a>Modello asincrono

La maggior parte delle operazioni nell'API dei servizi Web Windows può essere eseguita in modo sincrono o asincrono. Per chiamare una funzione in modo sincrono, passare un valore null per la struttura del [**\_ \_ contesto WS asincrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Per specificare che una funzione può essere eseguita in modo asincrono, passare un **\_ \_ contesto WS asincrono** non null alla funzione.

Quando viene chiamato in modo asincrono, una funzione può comunque essere completata in modo sincrono o asincrono. Se la funzione viene completata in modo sincrono, restituisce un valore che indica l'esito positivo o negativo finale e questo valore è sempre diverso da **WS \_ S \_ Async** (vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md)). Un valore restituito di **WS \_ S \_ Async**, tuttavia, indica che la funzione viene completata in modo asincrono. Quando la funzione viene completata in modo asincrono, viene richiamato un callback per segnalare il completamento dell'operazione. Questo callback indica il valore finale di esito positivo o negativo. Il callback non viene chiamato se l'operazione viene completata in modo sincrono.

Per creare un contesto asincrono, inizializzare i campi **callback** e **callbackState** della struttura del [**\_ \_ contesto WS asincrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Il campo **callbackState** viene usato per specificare un puntatore ai dati definiti dall'utente che vengono passati alla funzione [**di \_ \_ callback WS asincrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .

Nell'esempio seguente viene illustrata la chiamata di una funzione in modo asincrono passando un puntatore a una struttura del [**\_ \_ contesto WS asincrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) che contiene il callback e un puntatore ai dati di stato.

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

La struttura del [**\_ \_ contesto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asincrona viene utilizzata dalla funzione asincrona solo per la durata della chiamata di funzione (non per la durata dell'operazione asincrona), pertanto è possibile dichiararla in modo sicuro nello stack.

Se qualsiasi altro parametro, oltre alla struttura del [**\_ \_ contesto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asincrono, viene passato a una funzione asincrona come puntatori e la funzione viene completata in modo asincrono, è responsabilità del chiamante preservare i valori a cui puntano i parametri attivi (non liberati) fino a quando non viene richiamato il callback asincrono.

Esistono limitazioni sulle operazioni che possono essere eseguite da un callback. Per ulteriori informazioni sulle possibili operazioni, vedere il [**\_ \_ modello di callback WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

Quando si implementa una funzione asincrona, non richiamare il callback sullo stesso thread che ha chiamato la funzione asincrona prima che la funzione asincrona venisse restituita al chiamante, in quanto questa operazione interrompe il modello asincrono.

Quando si implementa una funzione che deve eseguire una serie di operazioni asincrone, provare a usare la funzione di supporto [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .

Nell' [esempio di funzione asincrona](asyncmodelexample.md) viene illustrato come implementare e utilizzare funzioni che seguono il modello asincrono.

L'avvio di un'operazione di i/o asincrona utilizza risorse di sistema. Se vengono avviate un numero sufficiente di operazioni di i/o, il sistema può smettere di rispondere. Per evitare questo problema, un'applicazione deve limitare il numero di operazioni asincrone che avvia.

Il modello asincrono utilizza gli elementi API seguenti.

| Callback                                         | Descrizione                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_callback asincrono \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | Il parametro della funzione di callback utilizzato con il modello asincrono.                                                                     |
| [**\_funzione ws Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Utilizzato con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) per specificare la funzione successiva da richiamare in una serie di operazioni asincrone. |



 



| Enumerazione                                      | Descrizione                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_modello di callback WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Specifica il comportamento di threading di un callback (ad esempio, [**un \_ \_ callback WS asincrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Funzione                                 | Descrizione                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Richiama un callback definito dall'utente che può avviare un'operazione asincrona e indicare una funzione che deve essere chiamata quando l'operazione asincrona è stata completata. |



 



| Struttura                                          | Descrizione                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contesto asincrono \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Specifica il callback asincrono e un puntatore ai dati definiti dall'utente, che verranno passati al callback asincrono.            |
| [**\_operazione asincrona \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Utilizzato con [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) per specificare la funzione successiva da richiamare in una serie di operazioni asincrone. |
| [**\_stato asincrono \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Usato da [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) per gestire lo stato di un'operazione asincrona.                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di funzione asincrona](asyncmodelexample.md)
</dt> <dt>

[**\_callback asincrono \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**\_contesto asincrono \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**\_modello di callback WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




