---
title: Stato utente host del servizio
description: L'host del servizio consente a un'applicazione di associare i dati sullo stato con ambito a livello di host del servizio.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Servizi Web di stato dell'host utente per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04530b74ef1ab0125b31e56751cdd6cec8109711f603c909f3afeb66970f081a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192431"
---
# <a name="service-host-user-state"></a>Stato utente host del servizio

[L'host del](service-host.md) servizio consente a un'applicazione di associare i dati sullo stato con ambito a livello di host del servizio. Questo stato viene specificato da una struttura [**WS \_ SERVICE \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) che viene passata alla funzione [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) quando l'applicazione crea un [host del](service-host.md)servizio , come illustrato nell'esempio seguente.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


I dati sullo stato sono disponibili per tutti i callback dell'host del servizio e le [operazioni del servizio](service-operation.md). I callback e le operazioni del servizio recuperano le informazioni chiamando la funzione [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) e specificando il contesto, a cui fa riferimento la struttura [WS \_ OPERATION \_ CONTEXT,](ws-operation-context.md) e la proprietà di contesto, come uno dei valori dell'enumerazione [**WS \_ OPERATION CONTEXT PROPERTY HOST USER \_ \_ \_ \_ \_ STATE,**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) come illustrato nell'esempio seguente.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




