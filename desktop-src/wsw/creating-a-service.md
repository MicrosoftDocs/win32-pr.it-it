---
title: Creazione di un servizio
description: La creazione di un servizio Web è notevolmente semplificata in WWSAPI dall'API del modello di servizio e dallo WsUtil.exe web.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f6daadbfcd1d06f76bf5bef97559214e36015d3f72ff440e77f4293a47ea57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805741"
---
# <a name="creating-a-service"></a>Creazione di un servizio

La creazione di un servizio Web è notevolmente semplificata in WWSAPI dall'API [del](service-model-layer-overview.md) modello di servizio e dallo [WsUtil.exe](wsutil-compiler-tool.md) web. Il modello di servizio fornisce un'API che consente al servizio e al client di inviare e ricevere [messaggi](message.md) tramite un [canale](channel.md) come chiamate al metodo C. Lo strumento WsUtil genera stub e intestazioni per l'implementazione del servizio.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implementazione di un servizio Calcolatrice con WWSAPI

Usando le origini generate dallo [ strumentoWsutil.exe, ](wsutil-compiler-tool.md) implementare il servizio seguendo questa procedura.

Includere le intestazioni nell'origine dell'applicazione.

``` syntax
#include "CalculatorProxyStub.h"
```

Implementare le operazioni del servizio. In questo esempio le operazioni del servizio sono le funzioni Add e Subtract del servizio calculator.

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

Definire il contratto di servizio impostando i campi di una [**struttura WS \_ SERVICE \_ CONTRACT.**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

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

Per un'implementazione completa del servizio calcolatrice, vedere l'esempio di codice in [HttpCalculatorServiceExample.](httpcalculatorserviceexample.md)

 

 




