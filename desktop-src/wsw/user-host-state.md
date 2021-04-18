---
title: Stato utente host del servizio
description: L'host del servizio consente a un'applicazione di associare i dati di stato che hanno come ambito il livello host del servizio.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Servizi Web per lo stato dell'host utente per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300702"
---
# <a name="service-host-user-state"></a>Stato utente host del servizio

L' [host del servizio](service-host.md) consente a un'applicazione di associare i dati di stato che hanno come ambito il livello host del servizio. Questo stato viene specificato da una struttura [**di \_ \_ Proprietà WS Service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) che viene passata alla funzione [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) quando l'applicazione crea un [host del servizio](service-host.md), come illustrato nell'esempio seguente.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


I dati relativi allo stato sono disponibili per tutti i callback dell'host del servizio e [le operazioni del servizio](service-operation.md). I callback e le operazioni del servizio recuperano le informazioni chiamando la funzione [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) e specificando il contesto, a cui fa riferimento la struttura del [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) e la proprietà di contesto, come uno dei valori della [**proprietà di \_ contesto dell'operazione \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, come illustrato nell'esempio seguente.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




