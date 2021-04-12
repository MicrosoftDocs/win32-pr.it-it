---
title: Creazione di un client
description: La creazione di un client per i servizi Web è molto semplificata in WWSAPI dall'API del modello di servizio e dallo strumento WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396851"
---
# <a name="creating-a-client"></a>Creazione di un client

La creazione di un client per i servizi Web è molto semplificata in WWSAPI dall'API del [modello di servizio](service-model-layer-overview.md) e dallo strumento [WsUtil.exe](wsutil-compiler-tool.md) . Il modello di servizio fornisce un'API che consente al client di inviare e ricevere [messaggi](message.md) tramite un [canale](channel.md) come chiamate al metodo C. Lo strumento WsUtil genera intestazioni e helper per l'implementazione del client. Queste intestazioni includono i tipi e i prototipi di funzione per le funzioni C che rappresentano i servizi offerti dal servizio Web di destinazione. Gli helper vengono utilizzati per creare il proxy del servizio, che contiene le informazioni di associazione e l' [indirizzo endpoint](endpoint-address.md) per il servizio.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Uso di WsUtil per generare intestazioni e helper

Per generare le intestazioni e gli helper, WsUtil apre e legge i file di metadati per il servizio di destinazione, ovvero i file WSDL e XSD, e li converte in intestazioni. Pertanto, è necessario recuperare i file di metadati per il servizio di destinazione in anticipo, ad esempio usando SvcUtil, una parte del Windows Communication Foundation. Per motivi di sicurezza, è fondamentale che le copie di questi file siano affidabili. Per ulteriori informazioni, vedere la sezione "sicurezza" dell'argomento dello [strumento del compilatore WsUtil](wsutil-compiler-tool.md) .

Per eseguire WsUtil, utilizzare la sintassi della riga di comando seguente se i file WSDL e XSD per il servizio si trovano nella propria directory: `WsUtil.exe *.wsdl *.xsd` . In alternativa, è possibile specificare i file in base al nome completo.

WsUtil genera in genere due file per ogni file di metadati: un'intestazione e un file C. Aggiungere questi file al progetto di codifica e usare \# le istruzioni include per includerli nel codice del client. I file XSD rappresentano i tipi e i file WSDL rappresentano le operazioni.

## <a name="creating-the-service-proxy"></a>Creazione del proxy del servizio

L'intestazione generata da WsUtil contiene una routine di supporto per la creazione del proxy del servizio con l'associazione necessaria. Questa routine è inclusa nella sezione "routine helper del criterio" del file di intestazione generato. Ad esempio, l'intestazione generata per il servizio di calcolatrice illustrato nell'esempio [httpcalculatorclientexample](httpcalculatorclientexample.md) conterrà il prototipo di funzione seguente.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorporare questo helper nel codice e passare un handle [del \_ \_ proxy del servizio WS](ws-service-proxy.md) per ricevere l'handle per il proxy del servizio creato. Nello scenario più semplice, in cui solo un handle del proxy del servizio e un oggetto Error vengono passati alla funzione, la chiamata ha un aspetto simile al seguente.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Per creare la parte dell'indirizzo del proxy del servizio, chiamare [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) con un handle per il proxy del servizio e un puntatore a un [**\_ \_ Indirizzo WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) che contiene l'indirizzo dell'endpoint del servizio a cui si desidera connettersi.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementazione del client con i prototipi di funzione

Le intestazioni generate dai file WSDL del servizio contengono anche i prototipi di funzione C che rappresentano i servizi disponibili dal servizio Web e specifici dell'associazione necessaria. Ad esempio, un'intestazione generata per il servizio di calcolatrice illustrato in HttpCalculatorServiceExample conterrà il prototipo seguente per l'operazione di moltiplicazione di tale servizio.

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

È possibile copiare i prototipi e usarli come modelli per codificare le chiamate di funzione nel client, in ogni caso passando l'handle al proxy del servizio. Al termine del proxy del servizio, chiamare [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).

 

 




