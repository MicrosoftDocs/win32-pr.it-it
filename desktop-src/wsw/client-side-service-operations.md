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
# <a name="client-side-service-operations"></a>Operazioni del servizio sul lato client

Di seguito è riportato il layout di un'operazione del servizio sul lato client:

-   [WS \_ \_Proxy del servizio](ws-service-proxy.md) \* serviceProxy: [proxy del servizio](service-proxy.md) per la chiamata.
-   [WS \_ Heap heap](ws-heap.md) \* : heap obbligatorio utilizzato per la serializzazione e la deserializzazione del corpo del [ \_ messaggio WS](ws-message.md).
-   Parametri delle operazioni di servizio: parametri relativi all'operazione del servizio.
-   [**Chiamare le proprietà e il relativo conteggio**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): una matrice di proprietà della chiamata.
-   [**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) Property Count: numero di proprietà della chiamata.
-   [**WS \_ \_Contesto**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asincrono asyncContext: contesto asincrono per l'esecuzione della chiamata in modo asincrono.
-   [WS \_ Errore:](ws-error.md) oggetto Rich Error.


### <a name="signature-for-client-side-service-operations"></a>Firma per le operazioni del servizio sul lato client

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

La chiamata all'operazione del servizio accetta un [ \_ heap WS](ws-heap.md) \* come parametro. Si tratta di un parametro obbligatorio utilizzato per la serializzazione/deserializzazione di corpi dei messaggi nei parametri.

L'applicazione deve chiamare [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) se la chiamata ha avuto esito positivo o meno. Se la chiamata ha esito positivo e presenta parametri in uscita, l'applicazione deve chiamare **WsResetHeap** immediatamente dopo che è stata completata con i parametri in uscita.

L'applicazione deve allocare memoria per i parametri in e out con [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). Potrebbe essere necessario riallocare il proxy del servizio in modo che i puntatori forniti vengano sovrascritti. Un tentativo di liberare tale memoria provocherà l'arresto anomalo dell'applicazione.

### <a name="client-side-service-operation-and-ws_heap"></a>Operazione del servizio lato client e \_ heap WS

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

### <a name="error-parameter"></a>Parametro error

L'applicazione deve sempre passare il parametro error a:

-   Ottenere informazioni dettagliate sugli errori se si verifica un errore durante la chiamata dell'operazione del servizio.
-   Ottenere l'oggetto errore se il servizio restituisce un errore. L'errore è contenuto nell'oggetto Error. In questo caso, il valore **HRESULT** restituito dall'operazione del servizio è **WS \_ E \_ endpoint \_ \_ received** (vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Proprietà delle chiamate per le operazioni del servizio sul lato client

Le proprietà di chiamata consentono a un'applicazione di specificare impostazioni personalizzate per una determinata chiamata. Attualmente, solo una proprietà di chiamata è disponibile con il modello di servizio, [**\_ \_ \_ \_ ID chiamata della proprietà WS Call**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

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

Spesso è preferibile abbandonare i risultati di una chiamata per restituire il controllo all'applicazione, in modo che il completamento effettivo della chiamata venga gestito dall'infrastruttura. Il proxy del servizio fornisce questa funzionalità tramite [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Si noti che il controllo per il chiamante non può essere restituito immediatamente, l'unica garanzia che il runtime del proxy del servizio fornisce è che non attende il completamento di un'operazione di I/O, prima di restituire il controllo al chiamante.

Le chiamate su un'operazione del servizio lato client possono essere abbandonate tramite una chiamata a [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall). Accetta un proxy del servizio e un ID chiamata. Un ID chiamata viene fornito come parte di una proprietà di chiamata in un'operazione del servizio.

Se l'ID chiamata è 0, il proxy del servizio abbandonerà tutte le chiamate in sospeso a tale istanza.

### <a name="call-timeouts"></a>Timeout delle chiamate

Per impostazione predefinita, un proxy del servizio ha un timeout di 30 secondi per ogni chiamata. Il timeout di una chiamata può essere modificato dalla proprietà del proxy del servizio di [**timeout delle chiamate della \_ \_ Proprietà WS \_ \_ proxy**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) durante la creazione di un proxy del servizio tramite [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).

Una volta raggiunto il timeout, la chiamata viene abbandonata.

### <a name="return-values"></a>Valori restituiti

Tutti i valori **HRESULT** di esito positivo devono essere considerati come esito positivo e tutti i valori di errore devono essere considerati come errori. Di seguito sono riportati alcuni dei valori **HRESULT** che un'applicazione può aspettarsi:

-   **WS \_ S \_ Async**: la chiamata verrà completata in modo asincrono.
-   NOERROR: la chiamata è stata completata correttamente.
-   **WS \_ \_Operazione E \_ abbandonata**: la chiamata è stata abbandonata. L'oggetto Error contiene il motivo dell'abbandono.
-   **WS \_ \_ \_ Operazione non valida**: il proxy del servizio non si trova in uno stato appropriato per effettuare una chiamata, controllare lo stato del proxy del servizio per determinare lo stato del proxy del servizio.

Per un elenco completo dei valori restituiti, vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md).

### <a name="code-examples"></a>Esempi di codice

Per esempi di codice, vedere gli argomenti seguenti:

-   [CallAbandonExample](callabandonexample.md)
-   [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




