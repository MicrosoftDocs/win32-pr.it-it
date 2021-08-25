---
title: Host del servizio
description: L'host del servizio è l'ambiente di runtime per l'hosting di un servizio all'interno di un processo.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Servizi Web host del servizio per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a09a41714ce80402c5430e6849988ae86163770af7ae3eb060fdd7925e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838667"
---
# <a name="service-host"></a>Host del servizio

L'host del servizio è l'ambiente di runtime per l'hosting di un servizio all'interno di un processo.


Un servizio può configurare uno o più endpoint all'interno di un host del servizio.

![Diagramma che mostra la struttura di un host del servizio contenente un endpoint di servizio.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Creazione di un host del servizio

Prima di creare un host del servizio, un servizio deve definire i relativi endpoint. Un endpoint nell'host del servizio è specificato nella struttura endpoint del servizio [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) ed è definito dalle informazioni seguenti:

-   Indirizzo, ovvero l'URI fisico in cui verrà ospitato il servizio.
-   Struttura [**WS \_ CHANNEL \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) che specifica il tipo del canale sottostante per l'endpoint.
-   Struttura [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) che specifica l'associazione del canale.
-   Struttura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) che contiene la descrizione di sicurezza per l'endpoint.
-   Struttura [**WS \_ SERVICE \_ CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) che rappresenta il [contratto di servizio per](contract.md) l'endpoint.
-   Struttura [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) che specifica una funzione di callback di autorizzazione per l'endpoint.
-   Struttura [**WS \_ SERVICE ENDPOINT \_ \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) che contiene una matrice di proprietà dell'endpoint di servizio.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

Sono supportati solo contratti unidirezionale per SOAP su UDP, rappresentati da [**WS \_ UDP CHANNEL \_ \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) nell'enumerazione **WS CHANNEL \_ \_ BINDING.**

Dopo la definizione, un endpoint può essere passato alla funzione [**WsCreateServiceHost,**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) che accetta una matrice di puntatori alle strutture endpoint del servizio [**WS. \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Un'applicazione può facoltativamente fornire una matrice di proprietà [**del servizio**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) a [**WsCreateServiceHost per**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) configurare impostazioni personalizzate nell'host del servizio.

Un'applicazione apre l'host del servizio per avviare l'accettazione delle richieste client.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Dopo aver aperto l'host del servizio, l'applicazione può chiuderlo se non sono presenti altre operazioni che lo richiedono. Si noti che non rilascia le risorse e che può essere riaperto con una chiamata successiva a [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Dopo la chiusura dell'host del servizio, un'applicazione può reimpostare l'host del servizio per il riutilizzo.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Quando l'applicazione viene eseguita con l'host del servizio, può liberare le risorse associate all'host del servizio chiamando la [**funzione WsFreeServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) Si noti [**che WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) deve essere chiamato prima di chiamare questa funzione.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Per informazioni sul collegamento di uno stato personalizzato all'host del servizio, vedere [Stato dell'host utente](user-host-state.md)

Per informazioni sull'autorizzazione in un host del servizio per un determinato endpoint, vedere [Autorizzazione del servizio](service-authorization.md).

Per informazioni sull'implementazione di operazioni del servizio e contratti di servizio per un servizio, vedere gli argomenti relativi alle operazioni [del](server-side-service-operations.md) servizio e [ai contratti di](contract.md)servizio.

## <a name="security"></a>Sicurezza

Un'applicazione può usare le proprietà seguenti per controllare la quantità di risorse allocate dall'host del servizio per conto dell'applicazione:

-   [**WS \_ PROPRIETÀ \_ \_ DELL'ENDPOINT \_ DI SERVIZIO MAX \_ ACCEPTING \_ CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ PROPRIETÀ \_ \_ DELL'ENDPOINT DI SERVIZIO \_ MAX \_ CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ PROPRIETÀ \_ \_ DELL'ENDPOINT \_ DI SERVIZIO MAX \_ CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ DIMENSIONI \_ MASSIME \_ HEAP DEL CORPO \_ \_ DELL'ENDPOINT \_ DI \_ SERVIZIO**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ PROPRIETÀ \_ DELL'ENDPOINT \_ DI SERVIZIO DIMENSIONI \_ \_ MASSIME POOL DI \_ \_ CHIAMATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ PROPRIETÀ \_ DELL'ENDPOINT \_ DI SERVIZIO DIMENSIONI \_ \_ MASSIME DEL POOL DI \_ \_ CANALI**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).

Le impostazioni predefinite sicure vengono scelte per ognuna di queste proprietà. Un'applicazione deve prestare attenzione se vuole modificare queste proprietà. Oltre alle proprietà indicate in precedenza, [l'applicazione](channel.md)può modificare anche le proprietà specifiche del canale, del [listener](listener.md) e del messaggio. [](message.md) Fare riferimento alle considerazioni sulla sicurezza di questi componenti prima di modificare una di queste impostazioni.

Inoltre, quando si usa l'API host del servizio WWSAPI, è necessario valutare attentamente le considerazioni seguenti sulla progettazione dell'applicazione:

-   Quando si usa MEX, le applicazioni devono prestare attenzione a non divulgare dati sensibili. Come mitigazione, se la natura dei dati esposti tramite MEX è sensibile, le applicazioni possono scegliere di configurare l'endpoint MEX con un'associazione sicura che richiede almeno l'autenticazione e implementare l'autorizzazione come parte dell'endpoint usando [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Per impostazione predefinita, le informazioni dettagliate sugli errori tramite errori sono disabilitate nell'host del servizio dalla proprietà FAULT DISCLOSURE delle proprietà del servizio [**WS. \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) È a discrezione dell'applicazione inviare informazioni dettagliate sull'errore come parte dell'errore. Tuttavia, ciò può comportare la diffusione di informazioni ed è pertanto consigliabile modificare questa impostazione solo per gli scenari di debug.
-   Oltre alla convalida eseguita per Basic Profile 2.0 e la serializzazione XML, l'host del servizio non esegue alcuna convalida sul contenuto dei dati ricevuto come parte dei parametri dell'operazione del servizio. È responsabilità dell'applicazione eseguire di per sé tutte le convalide dei parametri.
-   L'autorizzazione non viene implementata come parte dell'host del servizio. Tuttavia, le applicazioni possono implementare il proprio schema di autorizzazione [**usando WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e [**WS SERVICE SECURITY \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   È responsabilità dell'applicazione usare associazioni protette nel relativo endpoint. L'host del servizio non fornisce alcuna sicurezza oltre a quanto configurato nell'endpoint.

Gli elementi API seguenti vengono usati con l'host del servizio.

| Callback                                                                             | Descrizione                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**CALLBACK DEL \_ CANALE \_ ACCEPT DEL \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Richiamato quando un canale viene accettato in un listener dell'endpoint dall'host del servizio. |
| [**CALLBACK DEL \_ CANALE DI CHIUSURA DEL \_ \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Richiamato quando un canale viene chiuso o interrotto in un endpoint.                     |



 



| Enumerazione                                                                    | Descrizione                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**ID PROPRIETÀ \_ \_ ENDPOINT \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Parametri facoltativi per la configurazione di [**un ENDPOINT DEL \_ SERVIZIO \_ WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) |
| [**STATO HOST DEL SERVIZIO WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Stati in cui può essere presente un host del servizio.                                                   |
| [**ID PROPRIETÀ \_ DEL \_ SERVIZIO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Parametri facoltativi per la configurazione dell'host del servizio.                                       |



 



| Funzione                                                     | Descrizione                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Interrompe e interrompe le operazioni correnti nell'host del servizio.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Chiude tutti i listener in modo che non siano accettati nuovi canali dal client.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Crea un host del servizio.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Rilascia la memoria associata a un oggetto host del servizio.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Recupera una proprietà dell'host del servizio specificata.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Apre un host del servizio per la comunicazione e avvia i listener in tutti gli endpoint.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Reimposta l'host del servizio per il riutilizzo e reimposta il canale sottostante e i listener per il riutilizzo. |



 



| Handle                                       | Descrizione                                      |
|----------------------------------------------|--------------------------------------------------|
| [**HOST DEL SERVIZIO WS \_ \_**](ws-service-host.md) | Tipo opaco utilizzato per fare riferimento a un host del servizio. |



 



| Struttura                                                                              | Descrizione                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**ENDPOINT DI SERVIZIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Rappresenta un singolo endpoint in un host del servizio.                            |
| [**PROPRIETÀ \_ \_ DELL'ENDPOINT DEL \_ SERVIZIO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Specifica un'impostazione specifica del servizio.                                           |
| [**PROPRIETÀ DEL SERVIZIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Specifica un'impostazione specifica del servizio.                                           |
| [**CALLBACK ACCEPT \_ \_ DELLA PROPRIETÀ DEL \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Specifica il callback che viene chiamato quando un canale viene accettato correttamente. |
| [**CALLBACK DI \_ CHIUSURA DELLA PROPRIETÀ DEL \_ \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Specifica il callback che viene chiamato quando un canale sta per essere chiuso.    |



 

 

 




