---
title: Operazioni del servizio lato server
description: In questa sezione vengono descritte le operazioni del servizio sul lato servizio.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Server Side Service Operations Web Services for Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1656e56df08d00a0551946c4e52898beccd4d1a37a5bd96c63eb2066928fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344631"
---
# <a name="server-side-service-operations"></a>Operazioni del servizio lato server

In questa sezione vengono descritte le operazioni del servizio sul lato servizio.


Di seguito è riportato il layout di un'operazione del servizio lato server

-   const [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) \* context: contesto dell'operazione . [](context.md)
-   Parametri delle operazioni del servizio: parametri relativi all'operazione del servizio.
-   const [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contesto asincrono per l'esecuzione asincrona delle operazioni del servizio.
-   [WS \_ Errore](ws-error.md) \* DI ERRORE: oggetto errore rtf.

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

Il lato server deve usare gli errori per recapitare le condizioni di errore al client. A tale scopo, restituire un HRESULT non riuscito e incorporare l'errore nell'oggetto errore.

Se l'errore non è impostato sull'oggetto errore e viene restituito un HRESULT di errore, l'infrastruttura tenterà di restituire un errore al client. Il livello di dettagli divulgato al client in questo caso è controllato dalla proprietà del servizio [**WS \_ SERVICE FAULT \_ \_ \_ DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) nell'host [del servizio](service-host.md).

## <a name="call-completion"></a>Completamento delle chiamate

Una chiamata a un'operazione sincrona sul lato server viene chiamata come completa quando una delle due operazioni ha restituito il controllo all'host del servizio. Per un'operazione di servizio asincrona, una chiamata viene considerata completa dopo l'emissione della notifica di callback da parte dell'implementazione dell'operazione del servizio.

## <a name="call-lifetime"></a>Durata delle chiamate

È necessario fare particolare attenzione quando si implementa un'operazione del servizio lato server per la relativa durata. La durata di una chiamata può influire notevolmente sul tempo necessario all'arresto dell'host del servizio.

Se si prevede che un'operazione del servizio lato server si blocchi a causa di un'operazione associata a I/O, è consigliabile registrare un callback di annullamento in modo da ricevere una notifica quando l'host del servizio viene interrotto o quando la connessione sottostante viene chiusa dal client.

## <a name="server-side-service-operations-and-memory-consideration"></a>Considerazioni sulle operazioni sul lato server e sulla memoria

Se un'operazione del servizio deve allocare memoria per i parametri in uscita, deve usare l'oggetto [ \_ HEAP WS](ws-heap.md) disponibile tramite [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md).

Esempio: Operazione del servizio e HEAP \_ WS

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

-   WS \_ S \_ ASYNC: la chiamata verrà completata asincrona.
-   WS \_ S END: chiamata completata. Il server non prevede alcun messaggio \_ [WS \_ ](ws-message.md) dal client oltre questa chiamata. Se arriva un \_ altro messaggio WS, il server deve interrompere il canale.
-   NOERROR/Tutti gli altri HRESULTS riusciti: chiamata completata. Si noti che è consigliabile che l'applicazione non restituirà HRESULT altro quindi NOERROR per il corretto completamento dell'operazione del servizio.
-   Tutto ciò che ha un HRESULT di errore: un errore viene restituito al client se disponibile in WS \_ ERROR. In caso contrario, un errore generico viene inviato al client. Vedere la discussione sull'errore precedente.

Vedere [Annullamento delle chiamate](call-cancellation.md).

 

 




