---
title: Creazione di un client
description: La creazione di un client per i servizi Web è notevolmente semplificata in WWSAPI dall'API del modello di servizio e dallo WsUtil.exe servizio.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ca04ef5fbbeef76cd32a0b6523391deb19957479cd5f332715972f3b5bfbc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026559"
---
# <a name="creating-a-client"></a>Creazione di un client

La creazione di un client per i servizi Web [](service-model-layer-overview.md) è notevolmente semplificata in WWSAPI dall'API del modello di servizio e dallo [WsUtil.exe](wsutil-compiler-tool.md) servizio. Il modello di servizio fornisce un'API che consente al client di inviare e ricevere [messaggi](message.md) su un [canale come](channel.md) chiamate al metodo C. Lo strumento WsUtil genera intestazioni e helper per l'implementazione del client. Queste intestazioni includono i tipi e i prototipi di funzione per le funzioni C che rappresentano i servizi offerti dal servizio Web di destinazione. Gli helper vengono usati per creare il proxy del servizio, che contiene le informazioni di associazione e l'indirizzo [dell'endpoint](endpoint-address.md) per il servizio.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Uso di WsUtil per generare intestazioni e helper

Per generare le intestazioni e gli helper, WsUtil apre e legge i file di metadati per il servizio di destinazione, ovvero i file wsdl e xsd, e li converte in intestazioni. Pertanto, è necessario recuperare in anticipo i file di metadati per il servizio di destinazione, ad esempio usando SvcUtil, una parte di Windows Communication Foundation. Per motivi di sicurezza, è fondamentale che le copie di questi file siano attendibili. Per altre informazioni, vedere la sezione "Security" dell'argomento [WsUtil Compiler Tool.](wsutil-compiler-tool.md)

Per eseguire WsUtil, utilizzare la sintassi della riga di comando seguente se i file WSDL e XSD per il servizio sono nella propria directory: `WsUtil.exe *.wsdl *.xsd` . In alternativa, è possibile specificare i file in base al nome completo.

WsUtil genera in genere due file per ogni file di metadati: un'intestazione e un file C. Aggiungere questi file al progetto di codice e usare le istruzioni include per \# includerli nel codice per il client. I file XSD rappresentano i tipi e i file WSDL rappresentano le operazioni.

## <a name="creating-the-service-proxy"></a>Creazione del proxy del servizio

L'intestazione generata da WsUtil contiene una routine helper per la creazione del proxy del servizio con l'associazione richiesta. Questa routine è inclusa nella sezione "Routine helper criteri" del file di intestazione generato. Ad esempio, l'intestazione generata per il servizio calculator illustrata nell'esempio [httpcalculatorclientexample](httpcalculatorclientexample.md) conterrà il prototipo di funzione seguente.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorporare questo helper nel codice e passare un handle [proxy WS \_ SERVICE \_ ](ws-service-proxy.md) per ricevere l'handle al proxy del servizio creato. Nello scenario più semplice, in cui alla funzione vengono passati solo un handle del proxy del servizio e un oggetto errore, la chiamata è simile alla seguente.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Per creare la parte relativa all'indirizzo del proxy del servizio, chiamare [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) con un handle per il proxy del servizio e un puntatore a un indirizzo [**endpoint WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenente l'indirizzo dell'endpoint del servizio a cui ci si vuole connettere.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementazione del client con prototipi di funzione

Le intestazioni generate dai file WSDL del servizio contengono anche prototipi di funzione C che rappresentano i servizi disponibili dal servizio Web e specifici dell'associazione richiesta. Ad esempio, un'intestazione generata per il servizio calcolatrice illustrata in HttpCalculatorServiceExample conterrà il prototipo seguente per l'operazione di moltiplicazione del servizio.

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

È possibile copiare i prototipi e usarli come modelli per codificare le chiamate di funzione nel client, in ogni caso passando l'handle al proxy del servizio. Al termine dell'esecuzione del proxy del servizio, [**chiamare WsCloseServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)

 

 




