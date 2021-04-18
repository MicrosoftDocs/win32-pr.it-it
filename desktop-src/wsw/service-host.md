---
title: Host del servizio
description: L'host del servizio è l'ambiente di runtime per l'hosting di un servizio all'interno di un processo.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Servizi Web host servizio per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320441"
---
# <a name="service-host"></a>Host del servizio

L'host del servizio è l'ambiente di runtime per l'hosting di un servizio all'interno di un processo.


Un servizio può configurare uno o più endpoint all'interno di un host del servizio.

![Diagramma che illustra la struttura di un host del servizio contenente un endpoint del servizio.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Creazione di un host del servizio

Prima di creare un host del servizio, un servizio deve definire gli endpoint. Un endpoint nell'host del servizio viene specificato nella struttura dell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) ed è definito dalle informazioni seguenti:

-   Un indirizzo, ovvero l'URI fisico in cui verrà ospitato il servizio.
-   Struttura [**del \_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) che specifica il tipo del canale sottostante per l'endpoint.
-   Struttura [**di \_ \_ associazione WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) che specifica l'associazione del canale.
-   Struttura [**di \_ \_ Descrizione della sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) che contiene la descrizione di sicurezza per l'endpoint.
-   Struttura [**del \_ \_ contratto di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) che rappresenta il [contratto di servizio](contract.md) per l'endpoint.
-   Struttura [**di \_ \_ \_ callback di sicurezza del servizio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) che specifica una funzione di callback di autorizzazione per l'endpoint.
-   Struttura [**di \_ \_ \_ proprietà dell'endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) che contiene una matrice di proprietà dell'endpoint del servizio.

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

Solo i contratti unidirezionali sono supportati per SOAP su UDP, rappresentati [**dall' \_ \_ \_ associazione di canale WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) nell'enumerazione **WS \_ Channel \_ Binding** .

Una volta definito, un endpoint può essere passato alla funzione [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , che accetta una matrice di puntatori alle strutture dell' [**\_ \_ endpoint WS Service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Un'applicazione può facoltativamente fornire una matrice di [**proprietà del servizio**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) a [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) per configurare le impostazioni personalizzate nell'host del servizio.

Un'applicazione apre l'host del servizio per iniziare ad accettare le richieste dei client.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Dopo l'apertura dell'host del servizio, l'applicazione può chiuderla se non sono presenti altre operazioni che lo richiedono. Si noti che questo non rilascia le risorse e che può essere riaperto con una chiamata successiva a [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Dopo la chiusura dell'host del servizio, un'applicazione può reimpostare l'host del servizio per il riutilizzo.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Quando l'applicazione viene eseguita con l'host del servizio, può liberare le risorse associate all'host del servizio chiamando la funzione [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) . Si noti che [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) deve essere chiamato prima di chiamare questa funzione.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Per informazioni sul connessione di uno stato personalizzato all'host del servizio, vedere [stato host utente](user-host-state.md)

Per informazioni sull'autorizzazione in un host del servizio per un determinato endpoint, vedere [autorizzazione del servizio](service-authorization.md).

Per iInformation sull'implementazione di operazioni di servizio e contratti di servizio per un servizio, vedere gli argomenti relativi a [operazioni di servizio](server-side-service-operations.md) e [contratto di servizio](contract.md).

## <a name="security"></a>Sicurezza

Un'applicazione può utilizzare le proprietà seguenti per controllare la quantità di risorse allocate dall'host del servizio per conto dell'applicazione:

-   [**WS \_ \_proprietà endpoint \_ servizio \_ Max \_ accepting \_ Channels**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ concorrenza massima della proprietà dell'endpoint di servizio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ canale massimo proprietà endpoint servizio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ \_ \_ dimensioni massime heap del corpo della proprietà dell'endpoint servizio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_proprietà endpoint servizio- \_ \_ dimensioni massime \_ \_ pool \_ di chiamate**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ \_ \_ dimensioni massime pool di canali**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)per la proprietà dell'endpoint di servizio.

Per ognuna di queste proprietà si scelgono impostazioni predefinite sicure, un'applicazione deve essere attenta se desidera modificare queste proprietà. Oltre alle proprietà indicate sopra, il [canale](channel.md), il [listener](listener.md) e le proprietà specifiche del [messaggio](message.md) possono essere modificati anche dall'applicazione. Prima di modificare una di queste impostazioni, fare riferimento alle considerazioni sulla sicurezza di questi componenti.

Inoltre, quando si usa l'API dell'host del servizio WWSAPI, è consigliabile valutare attentamente le considerazioni di progettazione delle applicazioni seguenti:

-   Quando si utilizza MEX, le applicazioni devono prestare attenzione a non divulgare i dati sensibili. Come mitigazione, se la natura dei dati esposti tramite MEX è sensibile, le applicazioni possono scegliere di configurare l'endpoint MEX con un'associazione sicura che richiede almeno l'autenticazione e implementare l'autorizzazione come parte dell'endpoint utilizzando il callback di sicurezza del [**\_ servizio WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Per impostazione predefinita, le informazioni dettagliate sugli errori tramite errori sono disabilitate nell'host del servizio dalla proprietà di [**\_ \_ \_ \_ divulgazione degli errori della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) . È a discrezione dell'applicazione inviare informazioni dettagliate sugli errori come parte dell'errore. Tuttavia, ciò può comportare la divulgazione di informazioni ed è quindi consigliabile che questa impostazione venga modificata solo per gli scenari di debug.
-   Oltre alla convalida eseguita per il profilo di base 2,0 e la serializzazione XML, l'host del servizio non esegue alcuna convalida sul contenuto dati ricevuto come parte dei parametri dell'operazione del servizio. È responsabilità dell'applicazione eseguire autonomamente tutte le convalide dei parametri.
-   L'autorizzazione non è implementata come parte dell'host del servizio. Tuttavia, le applicazioni possono implementare il proprio schema di autorizzazione mediante [**WS \_ Security \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e il [**\_ callback di \_ sicurezza \_ del servizio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   È responsabilità dell'applicazione usare le associazioni sicure sul relativo endpoint. L'host del servizio non fornisce alcuna protezione oltre a quanto configurato nell'endpoint.

Gli elementi API seguenti vengono utilizzati con l'host del servizio.

| Callback                                                                             | Descrizione                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_ \_ \_ callback canale accettazione servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Richiamato quando un canale viene accettato su un listener dell'endpoint dall'host del servizio. |
| [**\_ \_ \_ callback canale chiusura servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Richiamato quando un canale viene chiuso o interrotto in un endpoint.                     |



 



| Enumerazione                                                                    | Descrizione                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_ \_ \_ ID proprietà endpoint servizio \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Parametri facoltativi per la configurazione di un [**\_ \_ endpoint di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint). |
| [**\_stato dell' \_ host del servizio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Gli stati in cui può trovarsi un host del servizio.                                                   |
| [**\_ \_ ID proprietà servizio \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Parametri facoltativi per la configurazione dell'host del servizio.                                       |



 



| Funzione                                                     | Descrizione                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Interrompe e sospende le operazioni correnti nell'host del servizio.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Chiude tutti i listener in modo che non vengano accettati nuovi canali dal client.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Consente di creare un host del servizio.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Rilascia la memoria associata a un oggetto host del servizio.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Recupera una proprietà dell'host del servizio specificata.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Apre un host del servizio per la comunicazione e avvia i listener su tutti gli endpoint.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Reimposta l'host del servizio per riutilizzarlo e reimposta il canale e i listener sottostanti per il riutilizzo. |



 



| Handle                                       | Descrizione                                      |
|----------------------------------------------|--------------------------------------------------|
| [**\_host del servizio WS \_**](ws-service-host.md) | Tipo opaco utilizzato per fare riferimento a un host del servizio. |



 



| Struttura                                                                              | Descrizione                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_endpoint servizio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Rappresenta un singolo endpoint in un host del servizio.                            |
| [**\_ \_ proprietà endpoint servizio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Specifica un'impostazione specifica del servizio.                                           |
| [**WS \_ Service ( \_ proprietà)**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Specifica un'impostazione specifica del servizio.                                           |
| [**\_ \_ \_ callback accetta proprietà servizio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Specifica il callback che viene chiamato quando un canale viene accettato correttamente. |
| [**\_ \_ \_ callback chiusura proprietà servizio \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Specifica il callback che viene chiamato quando un canale sta per essere chiuso.    |



 

 

 




