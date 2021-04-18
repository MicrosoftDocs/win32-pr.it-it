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
# <a name="service-host-user-state"></a><span data-ttu-id="3fda7-106">Stato utente host del servizio</span><span class="sxs-lookup"><span data-stu-id="3fda7-106">Service Host User State</span></span>

<span data-ttu-id="3fda7-107">L' [host del servizio](service-host.md) consente a un'applicazione di associare i dati di stato che hanno come ambito il livello host del servizio.</span><span class="sxs-lookup"><span data-stu-id="3fda7-107">The [service host](service-host.md) enables an application to associate state data that is scoped at the service-host level.</span></span> <span data-ttu-id="3fda7-108">Questo stato viene specificato da una struttura [**di \_ \_ Proprietà WS Service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) che viene passata alla funzione [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) quando l'applicazione crea un [host del servizio](service-host.md), come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="3fda7-108">This state is is specified by a [**WS\_SERVICE\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) structure that is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function when the application creates a [service host](service-host.md), as illustrated in the following example.</span></span>

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


<span data-ttu-id="3fda7-109">I dati relativi allo stato sono disponibili per tutti i callback dell'host del servizio e [le operazioni del servizio](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3fda7-109">The state data is available to all service host callbacks and [service operations](service-operation.md).</span></span> <span data-ttu-id="3fda7-110">I callback e le operazioni del servizio recuperano le informazioni chiamando la funzione [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) e specificando il contesto, a cui fa riferimento la struttura del [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) e la proprietà di contesto, come uno dei valori della [**proprietà di \_ contesto dell'operazione \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="3fda7-110">Callbacks and service operations retrieve the information by calling the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function and specifying the context, referenced by the [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure, and the context property, as one of the values of the [**WS\_OPERATION\_CONTEXT\_PROPERTY\_HOST\_USER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, as illustrated in the following example.</span></span>

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




