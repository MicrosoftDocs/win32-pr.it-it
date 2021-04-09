---
title: Creazione di un servizio
description: La creazione di un servizio Web è molto semplificata in WWSAPI dall'API del modello di servizio e dallo strumento WsUtil.exe.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856897"
---
# <a name="creating-a-service"></a>Creazione di un servizio

La creazione di un servizio Web è molto semplificata in WWSAPI dall'API del [modello di servizio](service-model-layer-overview.md) e dallo strumento [WsUtil.exe](wsutil-compiler-tool.md) . Il modello di servizio fornisce un'API che consente al servizio e al client di inviare e ricevere [messaggi](message.md) tramite un [canale](channel.md) come chiamate al metodo C. Lo strumento WsUtil genera stub e intestazioni per l'implementazione del servizio.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implementazione di un servizio di calcolatrice mediante WWSAPI

Utilizzando le origini generate dallo strumento [Wsutil.exe](wsutil-compiler-tool.md) , implementare il servizio attenendosi alla procedura seguente.

Includere le intestazioni nell'origine dell'applicazione.

``` syntax
#include "CalculatorProxyStub.h"
```

Implementare le operazioni del servizio. In questo esempio, le operazioni del servizio sono le funzioni di aggiunta e sottrazione del servizio calcolatrice.

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

Definire il contratto di servizio impostando i campi di una struttura del [**\_ \_ contratto di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

A questo punto, creare un host del servizio e aprirlo per la comunicazione.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

Per un'implementazione completa del servizio di calcolatrice, fare riferimento all'esempio di codice in [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) .

 

 




