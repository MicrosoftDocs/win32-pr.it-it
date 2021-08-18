---
title: Operazioni del servizio lato client
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 'Altre informazioni su: Operazioni del servizio sul lato client'
keywords:
- Servizi Web delle operazioni sul lato client per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657301"
---
# <a name="client-side-service-operations"></a>Operazioni del servizio lato client

Di seguito è riportato il layout di un'operazione del servizio lato client:

-   [WS \_ SERVICE \_ PROXY](ws-service-proxy.md) \* serviceProxy: [proxy del servizio](service-proxy.md) per la chiamata.
-   [WS \_ Heap](ws-heap.md) HEAP: heap necessario utilizzato per la serializzazione del corpo e \* la deserializzazione del [messaggio WS. \_ ](ws-message.md)
-   Parametri delle operazioni del servizio: parametri relativi all'operazione del servizio.
-   [**Proprietà di chiamata e relativo conteggio:**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)matrice di proprietà di chiamata.
-   [**Conteggio**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) delle proprietà di chiamata: numero di proprietà di chiamata.
-   [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: contesto asincrono per l'esecuzione asincrona della chiamata.
-   [WS \_ Errore](ws-error.md) DI ERRORE: oggetto errore rtf.


### <a name="signature-for-client-side-service-operations"></a>Firma per le operazioni del servizio lato client

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Considerazioni sulla memoria per le operazioni del servizio sul lato client

La chiamata all'operazione del servizio accetta un [ \_ heap WS](ws-heap.md) \* come parametro. Si tratta di un parametro obbligatorio usato per la serializzazione/deserializzazione dei corpi dei messaggi nei parametri.

L'applicazione deve [**chiamare WsResetHeap indipendentemente**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) dal fatto che la chiamata sia riuscita o meno. Se la chiamata ha esito positivo e ha parametri in uscita, l'applicazione deve chiamare **WsResetHeap** immediatamente dopo il termine con i parametri in uscita.

L'applicazione deve allocare memoria per i parametri in e out con [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). Il proxy del servizio potrebbe dover riallocarli in modo che i puntatori forniti verranno sovrascritti. Un tentativo di liberare tale memoria causerà l'arresto anomalo dell'applicazione.

### <a name="client-side-service-operation-and-ws_heap"></a>Operazione sul lato client del servizio e heap \_ WS

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

### <a name="error-parameter"></a>Parametro di errore

L'applicazione deve sempre passare il parametro error a:

-   Ottenere informazioni dettagliate sugli errori se si verifica un errore durante la chiamata all'operazione del servizio.
-   Ottenere l'oggetto errore se il servizio ha restituito un errore. L'errore è contenuto nell'oggetto errore. In questo caso, il **valore HRESULT** restituito dall'operazione del servizio è **WS \_ E ENDPOINT \_ FAULT \_ \_ RECEIVED** (vedere Windows [valori restituiti dei servizi Web).](windows-web-services-return-values.md)

### <a name="call-properties-for-client-side-service-operations"></a>Proprietà delle chiamate per le operazioni del servizio sul lato client

Le proprietà delle chiamate consentono a un'applicazione di specificare impostazioni personalizzate per una determinata chiamata. Attualmente è disponibile una sola proprietà call con il modello di [**servizio, WS \_ CALL PROPERTY CALL \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

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

### <a name="abandoning-a-call"></a>Abbandono di una chiamata

È spesso consigliabile abbandonare i risultati di una chiamata per rinunciare al controllo all'applicazione, in modo che il completamento effettivo della chiamata sia gestito dall'infrastruttura. Il proxy di servizio fornisce questa funzionalità [**tramite WsAbandonCall.**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

Si noti che il controllo al chiamante non può essere rimesso immediatamente, l'unica garanzia che il runtime del proxy del servizio garantisce è che non aspetterebbe il completamento di alcuna operazione associata all'I/O prima di dare il controllo al chiamante.

Le chiamate a un'operazione del servizio lato client possono essere abbandonate tramite una chiamata a [**WsAbandonCall.**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall) Accetta un proxy del servizio e un ID chiamata. Un ID chiamata viene specificato come parte delle proprietà di una chiamata in un'operazione del servizio.

Se l'ID chiamata è 0, il proxy del servizio abbandonerà tutte le chiamate in sospeso in tale istanza.

### <a name="call-timeouts"></a>Timeout delle chiamate

Per impostazione predefinita, un proxy del servizio ha un timeout di 30 secondi per ogni chiamata. Il timeout di una chiamata può essere modificato dalla proprietà proxy del servizio [**WS \_ PROXY CALL \_ \_ \_ TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) durante la creazione di un proxy del servizio [**tramite WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).

Dopo aver raggiunto un timeout, la chiamata viene abbandonata.

### <a name="return-values"></a>Valori restituiti

Tutti i valori **HRESULT** di esito positivo devono essere considerati come esito positivo e tutti i valori di errore devono essere considerati come errori. Di seguito sono riportati alcuni dei **valori HRESULT** previsti da un'applicazione:

-   **WS \_ S \_ ASYNC:** la chiamata verrà completata in modo asincrono.
-   NOERROR: chiamata completata.
-   **WS \_ E \_ OPERATION \_ ABANDONED:** la chiamata è stata abbandonata. L'oggetto errore contiene il motivo dell'abbandono.
-   **WS \_ E \_ OPERAZIONE \_ NON VALIDA:** il proxy del servizio non è in uno stato appropriato per effettuare una chiamata, controllare lo stato del proxy del servizio per capire lo stato del proxy del servizio.

Per un elenco completo dei valori restituiti, [Windows valori restituiti dei servizi Web](windows-web-services-return-values.md).

### <a name="code-examples"></a>Esempi di codice

Per esempi di codice, vedere quanto segue:

-   [CallAbandonExample](callabandonexample.md)
-   [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




