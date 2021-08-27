---
title: Context (Windows Web Services)
description: Un contesto viene usato nelle operazioni e nei callback del servizio del modello di servizio per passare i dati di stato pertinenti all'operazione o al callback del servizio quando viene richiamato.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Servizi Web di contesto per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7863f22193dd1496134afff991ff54efbee5026f2a11e52359b2b016c878c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026629"
---
# <a name="context-windows-web-services"></a>Context (Windows Web Services)

Un contesto viene utilizzato [](service-operation.md) nelle operazioni e nei callback del servizio del modello di servizio per passare i dati di stato pertinenti all'operazione o al callback del servizio quando viene richiamato. Una struttura [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) fa riferimento a un contesto. Le proprietà di un contesto possono essere recuperate con [**la funzione WsGetOperationContextProperty,**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) come illustrato nel codice seguente.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Non tutte le proprietà di contesto sono disponibili in un determinato momento. Vedere la documentazione relativa alla proprietà di contesto relativa alla disponibilità di una proprietà specifica in un callback o in [un'operazione del servizio](service-operation.md).

Per altre informazioni su come mantenere la durata e il threading del contesto dell'operazione, vedere l'argomento Durata e threading del contesto [dell'operazione.](operation-context-lifetime-and-threading.md)

L'enumerazione seguente fa parte del contesto:

-   [**ID DELLA \_ PROPRIETÀ DI \_ CONTESTO \_ \_ DELL'OPERAZIONE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

La funzione seguente fa parte del contesto:

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

L'handle seguente fa parte del contesto:

-   [CONTESTO \_ DELL'OPERAZIONE WS \_](ws-operation-context.md)

 

 




