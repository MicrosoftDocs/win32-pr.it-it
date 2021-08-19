---
title: Proxy del servizio
description: Un proxy del servizio è il proxy lato client per un servizio.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Servizi Web proxy di servizio per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff23349545c47dde2a54ea0b0911d3f792f21778f5053628929d3a98c69b0f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026185"
---
# <a name="service-proxy"></a>Proxy del servizio

Un proxy del servizio è il proxy lato client per un servizio. Il proxy del servizio consente alle applicazioni di inviare e ricevere [messaggi](message.md) su [un canale come](channel.md) chiamate al metodo .

I proxy del servizio vengono creati in base alle esigenze, aperti, usati per chiamare un servizio e chiusi quando non sono più necessari. In alternativa, un'applicazione può riusare un proxy del servizio per connettersi ripetutamente allo stesso servizio senza la spesa di tempo e risorse necessaria per inizializzare un proxy del servizio più di una volta. Il diagramma seguente illustra il flusso dei possibili stati del proxy del servizio e le chiamate di funzione o gli eventi che conducono da uno stato a un altro.

![Diagramma che mostra gli stati del proxy del servizio e le chiamate di funzione o gli eventi che conducono da uno stato a un altro.](images/serviceproxystates.png)

Questi stati del proxy di servizio vengono enumerati [**nell'enumerazione WS \_ SERVICE PROXY \_ \_ STATE.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state)

Come illustrato nel diagramma precedente e nel codice seguente, un proxy del servizio viene creato da una chiamata alla [**funzione WsCreateServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) Come parametri per questa chiamata, WWSAPI fornisce le enumerazioni seguenti:

-   [**TIPO DI CANALE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**BINDING DEL CANALE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Accetta anche parametri facoltativi usando i tipi di dati seguenti:

-   [**ID PROPRIETÀ PROXY WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**DESCRIZIONE DELLA SICUREZZA DI WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Dopo la creazione del proxy del servizio, la funzione **WsCreateServiceProxy** restituisce un riferimento al proxy del servizio, [WS \_ SERVICE \_ PROXY,](ws-service-proxy.md)tramite un parametro out.

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

Dopo aver creato il proxy del servizio, l'applicazione può aprire il proxy del servizio per [](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) la comunicazione con un servizio chiamando la funzione [**WsOpenServiceProxy,**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) passando una struttura di indirizzi contenente l'indirizzo di rete dell'endpoint del servizio a cui connettersi.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Quando il proxy del servizio è stato aperto, l'applicazione può usarlo per effettuare chiamate al servizio.

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

Quando l'applicazione non richiede più il proxy del servizio, chiude il proxy del servizio chiamando la [**funzione WsCloseServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) Libera anche la memoria associata chiamando [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

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

In alternativa, dopo aver chiamato [**WsCloseServiceProxy,**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) un'applicazione può riusare il proxy del servizio chiamando la [**funzione WsResetServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Per altre informazioni sull'uso dei proxy del servizio in contesti diversi, vedere gli argomenti seguenti:

-   [Proxy del servizio e sessioni](service-proxy-and-sessions.md)
-   [Operazione del servizio](service-operation.md)
-   [Operazioni del servizio lato client](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Sicurezza

Quando si usa l'API proxy del servizio WWSAPI, tenere presente attentamente le considerazioni di progettazione dell'applicazione seguenti:

-   Il proxy del servizio non eseguirà alcuna convalida dei dati oltre alla convalida di Basic Profile 2.0 e alla serializzazione XML. È responsabilità dell'applicazione convalidare i dati contenuti nei parametri che riceve come parte della chiamata.
-   La configurazione del numero massimo di chiamate in sospeso sul proxy del servizio, tramite il valore di enumerazione [**WS \_ PROXY PROPERTY \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) dell'enumerazione **WS \_ PROXY PROPERTY MAX \_ PENDING \_ \_ \_ CALLS,** fornisce protezione da un server a esecuzione lenta. Il valore massimo predefinito è 100. Le applicazioni devono prestare attenzione nella modifica delle impostazioni predefinite.
-   Il proxy del servizio non offre garanzie di sicurezza oltre a quelle specificate nella struttura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) usata per comunicare con il server.
-   Quando si modificano le impostazioni predefinite [del messaggio](message.md) e [del](channel.md) canale nel proxy del servizio, fare attenzione. Leggere le considerazioni sulla sicurezza associate ai messaggi e ai canali prima di modificare le proprietà correlate.
-   Il proxy del servizio crittografa tutte le credenziali conservate in memoria.

Gli elementi API seguenti sono correlati ai proxy del servizio.

| Callback                                                          | Descrizione                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DEI MESSAGGI PROXY WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Richiamato quando le intestazioni del messaggio di input stanno per essere inviate tramite o quando vengono appena ricevute le intestazioni di un messaggio di output. |



 



| Enumerazione                                                 | Descrizione                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**ID PROPRIETÀ CHIAMATA WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Enumera i parametri facoltativi per la configurazione di una chiamata in un'operazione del servizio lato client. |
| [**ID PROPRIETÀ PROXY WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Enumera i parametri facoltativi per la configurazione del proxy del servizio.                         |
| [**STATO DEL \_ \_ PROXY DEL \_ SERVIZIO WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | Stato del proxy del servizio.                                                           |



 



| Funzione                                                       | Descrizione                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abbandona una chiamata specificata su un proxy del servizio specificato.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Annulla tutti gli input e l'output in sospeso in un proxy del servizio specificato.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Solo interno. Serializza gli argomenti in un messaggio e lo invia tramite il canale. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Chiude un proxy del servizio per la comunicazione.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Crea un proxy del servizio.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Rilascia la memoria associata a un proxy del servizio.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Recupera una proprietà del proxy del servizio specificata.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Apre un proxy del servizio a un endpoint di servizio.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Reimposta il proxy del servizio.                                                             |



 



| Handle                                     | Descrizione                                       |
|--------------------------------------------|---------------------------------------------------|
| [PROXY DEL SERVIZIO WS \_ \_](ws-service-proxy.md) | Tipo opaco utilizzato per fare riferimento a un proxy del servizio. |



 



| Struttura                                         | Descrizione                 |
|---------------------------------------------------|-----------------------------|
| [**PROPRIETÀ CALL DI WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Specifica una proprietà di chiamata.  |
| [**WS \_ PROPRIETÀ \_ PROXY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Specifica una proprietà proxy. |



 

 

 




