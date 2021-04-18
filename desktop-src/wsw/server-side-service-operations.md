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
# <a name="server-side-service-operations"></a>Operazioni del servizio sul lato server

In questa sezione vengono descritte le operazioni del servizio sul lato servizio.


Di seguito è riportato il layout di un'operazione del servizio sul lato server

-   contesto [del \_ \_ contesto dell'operazione](ws-operation-context.md) const WS \* : il [contesto](context.md)dell'operazione.
-   Parametri delle operazioni di servizio: parametri relativi all'operazione del servizio.
-   const [**WS \_ Async \_ context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contesto asincrono per eseguire le operazioni del servizio in modo asincrono.
-   [WS \_ Errore](ws-error.md) \* : oggetto Rich Error.

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

## <a name="fault-and-error-handling"></a>Gestione degli errori e degli errori

Il lato server deve usare errori per recapitare le condizioni di errore al client. Questa operazione può essere eseguita restituendo un HRESULT con esito negativo e incorporando l'errore nell'oggetto Error.

Se l'errore non è impostato sull'oggetto Error e viene restituito un errore HRESULT, l'infrastruttura tenterà di recapitare un errore al client. Il livello dei dettagli divulgato al client in tal caso è controllato dalla proprietà del servizio [**di \_ \_ \_ \_ divulgazione degli errori della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) nell'host del [servizio](service-host.md).

## <a name="call-completion"></a>Completamento chiamata

Una chiamata a un'operazione di servizio lato server sincrona viene definita completa quando restituisce il controllo all'host del servizio. Per un'operazione asincrona del servizio, una chiamata viene considerata completa dopo che la notifica di callback viene rilasciata dall'implementazione dell'operazione del servizio.

## <a name="call-lifetime"></a>Durata chiamata

È necessario prestare particolare attenzione quando si implementa un'operazione del servizio sul lato server per la sua durata. La durata di una chiamata può influire significativamente sul tempo impiegato dall'host del servizio per l'arresto.

Se si prevede che un'operazione del servizio sul lato server si blocchi a causa di alcune operazioni di i/o associate, è consigliabile registrare un callback di annullamento in modo da ricevere una notifica in caso di interruzione dell'host del servizio o quando la connessione sottostante viene chiusa dal client.

## <a name="server-side-service-operations-and-memory-consideration"></a>Operazioni del servizio lato server e considerazione della memoria

Se un'operazione del servizio deve allocare memoria per i parametri in uscita, deve utilizzare l'oggetto dell' [ \_ heap WS](ws-heap.md) disponibile tramite il [ \_ \_ contesto dell'operazione WS](ws-operation-context.md).

Esempio: operazione del servizio e \_ heap WS

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

## <a name="return-values"></a>Valori restituiti

-   WS \_ S \_ Async: la chiamata verrà completata in Async.
-   WS \_ S \_ end: la chiamata è stata completata correttamente. il server non è in attesa di alcun [ \_ messaggio WS](ws-message.md) dal client oltre questa chiamata. Se \_ viene visualizzato un altro messaggio WS, il server deve interrompere il canale.
-   NOERROR/tutti gli altri HRESULT di esito positivo: la chiamata è stata completata correttamente. Si noti che è consigliabile che l'applicazione non restituisca HRESULT other quindi NOERROR per completare correttamente l'operazione del servizio.
-   Tutto con un errore HRESULT: viene restituito un errore al client se ne è disponibile uno in WS \_ Error. In caso contrario, un errore generico viene inviato di nuovo al client. Vedere la discussione sull'errore sopra.

Vedere, [chiamare l'annullamento](call-cancellation.md).

 

 




