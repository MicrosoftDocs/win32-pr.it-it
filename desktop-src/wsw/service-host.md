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
# <a name="service-host"></a><span data-ttu-id="927ba-106">Host del servizio</span><span class="sxs-lookup"><span data-stu-id="927ba-106">Service Host</span></span>

<span data-ttu-id="927ba-107">L'host del servizio è l'ambiente di runtime per l'hosting di un servizio all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="927ba-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="927ba-108">Un servizio può configurare uno o più endpoint all'interno di un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-108">A service can configure one or more endpoints inside a service host.</span></span>

![Diagramma che illustra la struttura di un host del servizio contenente un endpoint del servizio.](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="927ba-110">Creazione di un host del servizio</span><span class="sxs-lookup"><span data-stu-id="927ba-110">Creating a service host</span></span>

<span data-ttu-id="927ba-111">Prima di creare un host del servizio, un servizio deve definire gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="927ba-112">Un endpoint nell'host del servizio viene specificato nella struttura dell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) ed è definito dalle informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="927ba-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="927ba-113">Un indirizzo, ovvero l'URI fisico in cui verrà ospitato il servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="927ba-114">Struttura [**del \_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) che specifica il tipo del canale sottostante per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="927ba-115">Struttura [**di \_ \_ associazione WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) che specifica l'associazione del canale.</span><span class="sxs-lookup"><span data-stu-id="927ba-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="927ba-116">Struttura [**di \_ \_ Descrizione della sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) che contiene la descrizione di sicurezza per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="927ba-117">Struttura [**del \_ \_ contratto di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) che rappresenta il [contratto di servizio](contract.md) per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="927ba-118">Struttura [**di \_ \_ \_ callback di sicurezza del servizio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) che specifica una funzione di callback di autorizzazione per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="927ba-119">Struttura [**di \_ \_ \_ proprietà dell'endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) che contiene una matrice di proprietà dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

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

<span data-ttu-id="927ba-120">Solo i contratti unidirezionali sono supportati per SOAP su UDP, rappresentati [**dall' \_ \_ \_ associazione di canale WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) nell'enumerazione **WS \_ Channel \_ Binding** .</span><span class="sxs-lookup"><span data-stu-id="927ba-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="927ba-121">Una volta definito, un endpoint può essere passato alla funzione [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , che accetta una matrice di puntatori alle strutture dell' [**\_ \_ endpoint WS Service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .</span><span class="sxs-lookup"><span data-stu-id="927ba-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="927ba-122">Un'applicazione può facoltativamente fornire una matrice di [**proprietà del servizio**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) a [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) per configurare le impostazioni personalizzate nell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="927ba-123">Un'applicazione apre l'host del servizio per iniziare ad accettare le richieste dei client.</span><span class="sxs-lookup"><span data-stu-id="927ba-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="927ba-124">Dopo l'apertura dell'host del servizio, l'applicazione può chiuderla se non sono presenti altre operazioni che lo richiedono.</span><span class="sxs-lookup"><span data-stu-id="927ba-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="927ba-125">Si noti che questo non rilascia le risorse e che può essere riaperto con una chiamata successiva a [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span><span class="sxs-lookup"><span data-stu-id="927ba-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="927ba-126">Dopo la chiusura dell'host del servizio, un'applicazione può reimpostare l'host del servizio per il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="927ba-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="927ba-127">Quando l'applicazione viene eseguita con l'host del servizio, può liberare le risorse associate all'host del servizio chiamando la funzione [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) .</span><span class="sxs-lookup"><span data-stu-id="927ba-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="927ba-128">Si noti che [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) deve essere chiamato prima di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="927ba-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="927ba-129">Per informazioni sul connessione di uno stato personalizzato all'host del servizio, vedere [stato host utente](user-host-state.md)</span><span class="sxs-lookup"><span data-stu-id="927ba-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="927ba-130">Per informazioni sull'autorizzazione in un host del servizio per un determinato endpoint, vedere [autorizzazione del servizio](service-authorization.md).</span><span class="sxs-lookup"><span data-stu-id="927ba-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="927ba-131">Per iInformation sull'implementazione di operazioni di servizio e contratti di servizio per un servizio, vedere gli argomenti relativi a [operazioni di servizio](server-side-service-operations.md) e [contratto di servizio](contract.md).</span><span class="sxs-lookup"><span data-stu-id="927ba-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="927ba-132">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="927ba-132">Security</span></span>

<span data-ttu-id="927ba-133">Un'applicazione può utilizzare le proprietà seguenti per controllare la quantità di risorse allocate dall'host del servizio per conto dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="927ba-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="927ba-134">[**WS \_ \_proprietà endpoint \_ servizio \_ Max \_ accepting \_ Channels**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="927ba-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="927ba-135">[**WS \_ \_ \_ \_ \_ concorrenza massima della proprietà dell'endpoint di servizio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="927ba-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="927ba-136">[**WS \_ \_ \_ \_ \_ canale massimo proprietà endpoint servizio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="927ba-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="927ba-137">[**WS \_ \_ \_ \_ \_ \_ \_ dimensioni massime heap del corpo della proprietà dell'endpoint servizio**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="927ba-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="927ba-138">[**WS \_ \_proprietà endpoint servizio- \_ \_ dimensioni massime \_ \_ pool \_ di chiamate**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="927ba-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="927ba-139">[**WS \_ \_ \_ \_ \_ \_ \_ dimensioni massime pool di canali**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)per la proprietà dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="927ba-140">Per ognuna di queste proprietà si scelgono impostazioni predefinite sicure, un'applicazione deve essere attenta se desidera modificare queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="927ba-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="927ba-141">Oltre alle proprietà indicate sopra, il [canale](channel.md), il [listener](listener.md) e le proprietà specifiche del [messaggio](message.md) possono essere modificati anche dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="927ba-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="927ba-142">Prima di modificare una di queste impostazioni, fare riferimento alle considerazioni sulla sicurezza di questi componenti.</span><span class="sxs-lookup"><span data-stu-id="927ba-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="927ba-143">Inoltre, quando si usa l'API dell'host del servizio WWSAPI, è consigliabile valutare attentamente le considerazioni di progettazione delle applicazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="927ba-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="927ba-144">Quando si utilizza MEX, le applicazioni devono prestare attenzione a non divulgare i dati sensibili.</span><span class="sxs-lookup"><span data-stu-id="927ba-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="927ba-145">Come mitigazione, se la natura dei dati esposti tramite MEX è sensibile, le applicazioni possono scegliere di configurare l'endpoint MEX con un'associazione sicura che richiede almeno l'autenticazione e implementare l'autorizzazione come parte dell'endpoint utilizzando il callback di sicurezza del [**\_ servizio WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="927ba-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="927ba-146">Per impostazione predefinita, le informazioni dettagliate sugli errori tramite errori sono disabilitate nell'host del servizio dalla proprietà di [**\_ \_ \_ \_ divulgazione degli errori della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="927ba-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="927ba-147">È a discrezione dell'applicazione inviare informazioni dettagliate sugli errori come parte dell'errore.</span><span class="sxs-lookup"><span data-stu-id="927ba-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="927ba-148">Tuttavia, ciò può comportare la divulgazione di informazioni ed è quindi consigliabile che questa impostazione venga modificata solo per gli scenari di debug.</span><span class="sxs-lookup"><span data-stu-id="927ba-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="927ba-149">Oltre alla convalida eseguita per il profilo di base 2,0 e la serializzazione XML, l'host del servizio non esegue alcuna convalida sul contenuto dati ricevuto come parte dei parametri dell'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="927ba-150">È responsabilità dell'applicazione eseguire autonomamente tutte le convalide dei parametri.</span><span class="sxs-lookup"><span data-stu-id="927ba-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="927ba-151">L'autorizzazione non è implementata come parte dell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="927ba-152">Tuttavia, le applicazioni possono implementare il proprio schema di autorizzazione mediante [**WS \_ Security \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e il [**\_ callback di \_ sicurezza \_ del servizio WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="927ba-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="927ba-153">È responsabilità dell'applicazione usare le associazioni sicure sul relativo endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="927ba-154">L'host del servizio non fornisce alcuna protezione oltre a quanto configurato nell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="927ba-155">Gli elementi API seguenti vengono utilizzati con l'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="927ba-156">Callback</span><span class="sxs-lookup"><span data-stu-id="927ba-156">Callback</span></span>                                                                             | <span data-ttu-id="927ba-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="927ba-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="927ba-158">**\_ \_ \_ callback canale accettazione servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="927ba-159">Richiamato quando un canale viene accettato su un listener dell'endpoint dall'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="927ba-160">**\_ \_ \_ callback canale chiusura servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="927ba-161">Richiamato quando un canale viene chiuso o interrotto in un endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="927ba-162">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="927ba-162">Enumeration</span></span>                                                                    | <span data-ttu-id="927ba-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="927ba-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="927ba-164">**\_ \_ \_ ID proprietà endpoint servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="927ba-165">Parametri facoltativi per la configurazione di un [**\_ \_ endpoint di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="927ba-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="927ba-166">**\_stato dell' \_ host del servizio WS \_**</span><span class="sxs-lookup"><span data-stu-id="927ba-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="927ba-167">Gli stati in cui può trovarsi un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="927ba-168">**\_ \_ ID proprietà servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="927ba-169">Parametri facoltativi per la configurazione dell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="927ba-170">Funzione</span><span class="sxs-lookup"><span data-stu-id="927ba-170">Function</span></span>                                                     | <span data-ttu-id="927ba-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="927ba-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="927ba-172">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="927ba-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="927ba-173">Interrompe e sospende le operazioni correnti nell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="927ba-174">**WsCloseServiceHost**</span><span class="sxs-lookup"><span data-stu-id="927ba-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="927ba-175">Chiude tutti i listener in modo che non vengano accettati nuovi canali dal client.</span><span class="sxs-lookup"><span data-stu-id="927ba-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="927ba-176">**WsCreateServiceHost**</span><span class="sxs-lookup"><span data-stu-id="927ba-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="927ba-177">Consente di creare un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="927ba-178">**WsFreeServiceHost**</span><span class="sxs-lookup"><span data-stu-id="927ba-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="927ba-179">Rilascia la memoria associata a un oggetto host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="927ba-180">**WsGetServiceHostProperty**</span><span class="sxs-lookup"><span data-stu-id="927ba-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="927ba-181">Recupera una proprietà dell'host del servizio specificata.</span><span class="sxs-lookup"><span data-stu-id="927ba-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="927ba-182">**WsOpenServiceHost**</span><span class="sxs-lookup"><span data-stu-id="927ba-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="927ba-183">Apre un host del servizio per la comunicazione e avvia i listener su tutti gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="927ba-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="927ba-184">**WsResetServiceHost**</span><span class="sxs-lookup"><span data-stu-id="927ba-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="927ba-185">Reimposta l'host del servizio per riutilizzarlo e reimposta il canale e i listener sottostanti per il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="927ba-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="927ba-186">Handle</span><span class="sxs-lookup"><span data-stu-id="927ba-186">Handle</span></span>                                       | <span data-ttu-id="927ba-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="927ba-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="927ba-188">**\_host del servizio WS \_**</span><span class="sxs-lookup"><span data-stu-id="927ba-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="927ba-189">Tipo opaco utilizzato per fare riferimento a un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="927ba-190">Struttura</span><span class="sxs-lookup"><span data-stu-id="927ba-190">Structure</span></span>                                                                              | <span data-ttu-id="927ba-191">Descrizione</span><span class="sxs-lookup"><span data-stu-id="927ba-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="927ba-192">**\_endpoint servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="927ba-193">Rappresenta un singolo endpoint in un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="927ba-194">**\_ \_ proprietà endpoint servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="927ba-195">Specifica un'impostazione specifica del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="927ba-196">**WS \_ Service ( \_ proprietà)**</span><span class="sxs-lookup"><span data-stu-id="927ba-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="927ba-197">Specifica un'impostazione specifica del servizio.</span><span class="sxs-lookup"><span data-stu-id="927ba-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="927ba-198">**\_ \_ \_ callback accetta proprietà servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="927ba-199">Specifica il callback che viene chiamato quando un canale viene accettato correttamente.</span><span class="sxs-lookup"><span data-stu-id="927ba-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="927ba-200">**\_ \_ \_ callback chiusura proprietà servizio \_ WS**</span><span class="sxs-lookup"><span data-stu-id="927ba-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="927ba-201">Specifica il callback che viene chiamato quando un canale sta per essere chiuso.</span><span class="sxs-lookup"><span data-stu-id="927ba-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




