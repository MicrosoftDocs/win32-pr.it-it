---
title: Contesto (servizi Web Windows)
description: Un contesto viene utilizzato nelle operazioni del servizio del modello di servizio e nei callback per passare i dati sullo stato pertinente all'operazione del servizio o al callback quando viene richiamato.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Servizi Web di contesto per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103956089"
---
# <a name="context-windows-web-services"></a>Contesto (servizi Web Windows)

Un contesto viene utilizzato nelle operazioni del [servizio](service-operation.md) del modello di servizio e nei callback per passare i dati sullo stato pertinente all'operazione del servizio o al callback quando viene richiamato. Una struttura del [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) fa riferimento a un contesto. È possibile recuperare le proprietà di un contesto con la funzione [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , come illustrato nel codice seguente.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Non tutte le proprietà di contesto sono disponibili in un determinato momento. Vedere la documentazione relativa alla proprietà di contesto relativa alla disponibilità di una proprietà specifica in un'operazione di callback o di [servizio](service-operation.md).

Per ulteriori informazioni su come gestire la durata e il threading del contesto dell'operazione, vedere l'argomento relativo alla [durata e al threading del contesto dell'operazione](operation-context-lifetime-and-threading.md) .

L'enumerazione seguente fa parte del contesto:

-   [**\_ID della \_ proprietà di contesto dell'operazione WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

La funzione seguente fa parte del contesto:

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

Il seguente handle fa parte del contesto:

-   [\_contesto dell'operazione WS \_](ws-operation-context.md)

 

 




