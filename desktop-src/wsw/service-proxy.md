---
title: Proxy servizio
description: Un proxy del servizio è il proxy sul lato client per un servizio.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Servizi Web proxy servizio per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320448"
---
# <a name="service-proxy"></a>Proxy servizio

Un proxy del servizio è il proxy sul lato client per un servizio. Il proxy del servizio consente alle applicazioni di inviare e ricevere [messaggi](message.md) su un [canale](channel.md) come chiamate al metodo.

I proxy del servizio vengono creati in base alle esigenze, aperti, usati per chiamare un servizio e chiusi quando non sono più necessari. In alternativa, un'applicazione può riutilizzare un proxy del servizio per connettersi ripetutamente allo stesso servizio senza il dispendio di tempo e le risorse necessarie per inizializzare un proxy del servizio più di una volta. Il diagramma seguente illustra il flusso degli stati possibili del proxy del servizio e le chiamate di funzione o gli eventi che portano da uno stato a un altro.

![Diagramma che Mostra gli Stati del proxy del servizio e le chiamate di funzione o gli eventi che portano da uno stato a un altro.](images/serviceproxystates.png)

Questi Stati del proxy del servizio vengono enumerati nell'enumerazione [**\_ \_ \_ dello stato del proxy del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .

Come illustrato nel diagramma precedente e nel codice seguente, un proxy del servizio viene creato da una chiamata alla funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) . Come parametri per la chiamata, WWSAPI fornisce le enumerazioni seguenti:

-   [**\_tipo di canale WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**\_binding di canale WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Accetta inoltre parametri facoltativi utilizzando i tipi di dati seguenti:

-   [**\_ID della \_ proprietà del proxy WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**\_Descrizione della sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Quando il proxy del servizio è stato creato, la funzione **WsCreateServiceProxy** restituisce un riferimento al proxy del servizio, [WS \_ Service \_ proxy](ws-service-proxy.md), tramite un parametro out.

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

Al momento della creazione del proxy del servizio, l'applicazione può aprire il proxy del servizio per la comunicazione con un servizio chiamando la funzione [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , passando una struttura di [**indirizzi**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenente l'indirizzo di rete dell'endpoint del servizio a cui connettersi.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Quando il proxy del servizio è stato aperto, può essere utilizzato dall'applicazione per effettuare chiamate al servizio.

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

Quando l'applicazione non necessita più del proxy del servizio, chiude il proxy del servizio chiamando la funzione [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) . Consente inoltre di liberare la memoria associata chiamando [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a>Riutilizzo del proxy del servizio

In alternativa, dopo la chiamata a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , un'applicazione può riutilizzare il proxy del servizio chiamando la funzione [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Per ulteriori informazioni sull'utilizzo dei proxy servizio in contesti diversi, vedere gli argomenti seguenti:

-   [Proxy e sessioni del servizio](service-proxy-and-sessions.md)
-   [Operazione del servizio](service-operation.md)
-   [Operazioni del servizio lato client](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Sicurezza

Quando si usa l'API del proxy del servizio WWSAPI, è opportuno notare attentamente le considerazioni di progettazione delle applicazioni seguenti:

-   Il proxy del servizio non eseguirà alcuna convalida dei dati oltre la convalida di base del profilo 2,0 e la serializzazione XML. È responsabilità dell'applicazione convalidare i dati contenuti nei parametri ricevuti come parte della chiamata.
-   Configurare il numero massimo di chiamate in sospeso sul proxy del servizio usando il valore di enumerazione dell' [**\_ ID di \_ proprietà \_ del proxy**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) WS valore della **\_ Proprietà WS proxy \_ \_ Max \_ Pending \_ calls**, fornisce la protezione contro un server con esecuzione rallentata. Il valore massimo predefinito è 100. Per modificare le impostazioni predefinite, le applicazioni devono prestare particolare attenzione.
-   Il proxy del servizio non fornisce alcuna garanzia di sicurezza oltre a quelle specificate nella struttura di [**\_ \_ Descrizione della protezione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) utilizzata per comunicare con il server.
-   Prestare attenzione quando si modificano le impostazioni predefinite del [canale](channel.md) e del [messaggio](message.md) nel proxy del servizio. Leggere le considerazioni sulla sicurezza associate ai messaggi e ai canali prima di modificare le proprietà correlate.
-   Il proxy del servizio crittografa tutte le credenziali conservate in memoria.

Gli elementi API seguenti sono correlati ai proxy del servizio.

| Callback                                                          | Descrizione                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_callback del \_ messaggio WS proxy \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Richiamato quando le intestazioni del messaggio di input stanno per essere inviate tramite o quando vengono ricevute solo le intestazioni dei messaggi di output. |



 



| Enumerazione                                                 | Descrizione                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_ID della \_ proprietà di chiamata WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumera i parametri facoltativi per la configurazione di una chiamata a un'operazione del servizio lato client. |
| [**\_ID della \_ proprietà del proxy WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumera i parametri facoltativi per la configurazione del proxy del servizio.                         |
| [**\_stato del \_ proxy del servizio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | Stato del proxy del servizio.                                                           |



 



| Funzione                                                       | Descrizione                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abbandona una chiamata specificata su un proxy del servizio specificato.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Annulla tutti gli input e output in sospeso in un proxy del servizio specificato.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Solo interno. Serializza gli argomenti in un messaggio e lo invia sul canale. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Chiude un proxy del servizio per la comunicazione.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Crea un proxy del servizio.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Rilascia la memoria associata a un proxy del servizio.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Recupera una proprietà del proxy del servizio specificata.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Apre un proxy del servizio a un endpoint del servizio.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Reimposta il proxy del servizio.                                                             |



 



| Handle                                     | Descrizione                                       |
|--------------------------------------------|---------------------------------------------------|
| [\_proxy servizio \_ WS](ws-service-proxy.md) | Tipo opaco utilizzato per fare riferimento a un proxy del servizio. |



 



| Struttura                                         | Descrizione                 |
|---------------------------------------------------|-----------------------------|
| [**\_Proprietà WS Call \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Specifica una proprietà di chiamata.  |
| [**WS \_ \_proprietà del proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Specifica una proprietà del proxy. |



 

 

 




