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
# <a name="service-proxy"></a><span data-ttu-id="7f6eb-106">Proxy servizio</span><span class="sxs-lookup"><span data-stu-id="7f6eb-106">Service Proxy</span></span>

<span data-ttu-id="7f6eb-107">Un proxy del servizio è il proxy sul lato client per un servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="7f6eb-108">Il proxy del servizio consente alle applicazioni di inviare e ricevere [messaggi](message.md) su un [canale](channel.md) come chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="7f6eb-109">I proxy del servizio vengono creati in base alle esigenze, aperti, usati per chiamare un servizio e chiusi quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="7f6eb-110">In alternativa, un'applicazione può riutilizzare un proxy del servizio per connettersi ripetutamente allo stesso servizio senza il dispendio di tempo e le risorse necessarie per inizializzare un proxy del servizio più di una volta.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="7f6eb-111">Il diagramma seguente illustra il flusso degli stati possibili del proxy del servizio e le chiamate di funzione o gli eventi che portano da uno stato a un altro.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![Diagramma che Mostra gli Stati del proxy del servizio e le chiamate di funzione o gli eventi che portano da uno stato a un altro.](images/serviceproxystates.png)

<span data-ttu-id="7f6eb-113">Questi Stati del proxy del servizio vengono enumerati nell'enumerazione [**\_ \_ \_ dello stato del proxy del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="7f6eb-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="7f6eb-114">Come illustrato nel diagramma precedente e nel codice seguente, un proxy del servizio viene creato da una chiamata alla funzione [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="7f6eb-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="7f6eb-115">Come parametri per la chiamata, WWSAPI fornisce le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f6eb-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="7f6eb-116">**\_tipo di canale WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="7f6eb-117">**\_binding di canale WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="7f6eb-118">Accetta inoltre parametri facoltativi utilizzando i tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f6eb-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="7f6eb-119">**\_ID della \_ proprietà del proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="7f6eb-120">**\_Descrizione della sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="7f6eb-121">Quando il proxy del servizio è stato creato, la funzione **WsCreateServiceProxy** restituisce un riferimento al proxy del servizio, [WS \_ Service \_ proxy](ws-service-proxy.md), tramite un parametro out.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

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

<span data-ttu-id="7f6eb-122">Al momento della creazione del proxy del servizio, l'applicazione può aprire il proxy del servizio per la comunicazione con un servizio chiamando la funzione [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , passando una struttura di [**indirizzi**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenente l'indirizzo di rete dell'endpoint del servizio a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="7f6eb-123">Quando il proxy del servizio è stato aperto, può essere utilizzato dall'applicazione per effettuare chiamate al servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

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

<span data-ttu-id="7f6eb-124">Quando l'applicazione non necessita più del proxy del servizio, chiude il proxy del servizio chiamando la funzione [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="7f6eb-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="7f6eb-125">Consente inoltre di liberare la memoria associata chiamando [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="7f6eb-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

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

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="7f6eb-126">Riutilizzo del proxy del servizio</span><span class="sxs-lookup"><span data-stu-id="7f6eb-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="7f6eb-127">In alternativa, dopo la chiamata a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , un'applicazione può riutilizzare il proxy del servizio chiamando la funzione [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="7f6eb-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="7f6eb-128">Per ulteriori informazioni sull'utilizzo dei proxy servizio in contesti diversi, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f6eb-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="7f6eb-129">Proxy e sessioni del servizio</span><span class="sxs-lookup"><span data-stu-id="7f6eb-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="7f6eb-130">Operazione del servizio</span><span class="sxs-lookup"><span data-stu-id="7f6eb-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="7f6eb-131">Operazioni del servizio lato client</span><span class="sxs-lookup"><span data-stu-id="7f6eb-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="7f6eb-132">HttpCalculatorClientExample</span><span class="sxs-lookup"><span data-stu-id="7f6eb-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="7f6eb-133">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="7f6eb-133">Security</span></span>

<span data-ttu-id="7f6eb-134">Quando si usa l'API del proxy del servizio WWSAPI, è opportuno notare attentamente le considerazioni di progettazione delle applicazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f6eb-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="7f6eb-135">Il proxy del servizio non eseguirà alcuna convalida dei dati oltre la convalida di base del profilo 2,0 e la serializzazione XML.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="7f6eb-136">È responsabilità dell'applicazione convalidare i dati contenuti nei parametri ricevuti come parte della chiamata.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="7f6eb-137">Configurare il numero massimo di chiamate in sospeso sul proxy del servizio usando il valore di enumerazione dell' [**\_ ID di \_ proprietà \_ del proxy**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) WS valore della **\_ Proprietà WS proxy \_ \_ Max \_ Pending \_ calls**, fornisce la protezione contro un server con esecuzione rallentata.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="7f6eb-138">Il valore massimo predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-138">The default maximum is 100.</span></span> <span data-ttu-id="7f6eb-139">Per modificare le impostazioni predefinite, le applicazioni devono prestare particolare attenzione.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="7f6eb-140">Il proxy del servizio non fornisce alcuna garanzia di sicurezza oltre a quelle specificate nella struttura di [**\_ \_ Descrizione della protezione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) utilizzata per comunicare con il server.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="7f6eb-141">Prestare attenzione quando si modificano le impostazioni predefinite del [canale](channel.md) e del [messaggio](message.md) nel proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="7f6eb-142">Leggere le considerazioni sulla sicurezza associate ai messaggi e ai canali prima di modificare le proprietà correlate.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="7f6eb-143">Il proxy del servizio crittografa tutte le credenziali conservate in memoria.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="7f6eb-144">Gli elementi API seguenti sono correlati ai proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="7f6eb-145">Callback</span><span class="sxs-lookup"><span data-stu-id="7f6eb-145">Callback</span></span>                                                          | <span data-ttu-id="7f6eb-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f6eb-147">**\_callback del \_ messaggio WS proxy \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="7f6eb-148">Richiamato quando le intestazioni del messaggio di input stanno per essere inviate tramite o quando vengono ricevute solo le intestazioni dei messaggi di output.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="7f6eb-149">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-149">Enumeration</span></span>                                                 | <span data-ttu-id="7f6eb-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f6eb-151">**\_ID della \_ proprietà di chiamata WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="7f6eb-152">Enumera i parametri facoltativi per la configurazione di una chiamata a un'operazione del servizio lato client.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="7f6eb-153">**\_ID della \_ proprietà del proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="7f6eb-154">Enumera i parametri facoltativi per la configurazione del proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="7f6eb-155">**\_stato del \_ proxy del servizio WS \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="7f6eb-156">Stato del proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="7f6eb-157">Funzione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-157">Function</span></span>                                                       | <span data-ttu-id="7f6eb-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="7f6eb-159">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="7f6eb-160">Abbandona una chiamata specificata su un proxy del servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="7f6eb-161">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="7f6eb-162">Annulla tutti gli input e output in sospeso in un proxy del servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="7f6eb-163">**WsCall**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="7f6eb-164">Solo interno.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-164">Internal only.</span></span> <span data-ttu-id="7f6eb-165">Serializza gli argomenti in un messaggio e lo invia sul canale.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="7f6eb-166">**WsCloseServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="7f6eb-167">Chiude un proxy del servizio per la comunicazione.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="7f6eb-168">**WsCreateServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="7f6eb-169">Crea un proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="7f6eb-170">**WsFreeServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="7f6eb-171">Rilascia la memoria associata a un proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="7f6eb-172">**WsGetServiceProxyProperty**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="7f6eb-173">Recupera una proprietà del proxy del servizio specificata.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="7f6eb-174">**WsOpenServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="7f6eb-175">Apre un proxy del servizio a un endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="7f6eb-176">**WsResetServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="7f6eb-177">Reimposta il proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="7f6eb-178">Handle</span><span class="sxs-lookup"><span data-stu-id="7f6eb-178">Handle</span></span>                                     | <span data-ttu-id="7f6eb-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="7f6eb-180">\_proxy servizio \_ WS</span><span class="sxs-lookup"><span data-stu-id="7f6eb-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="7f6eb-181">Tipo opaco utilizzato per fare riferimento a un proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="7f6eb-182">Struttura</span><span class="sxs-lookup"><span data-stu-id="7f6eb-182">Structure</span></span>                                         | <span data-ttu-id="7f6eb-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f6eb-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="7f6eb-184">**\_Proprietà WS Call \_**</span><span class="sxs-lookup"><span data-stu-id="7f6eb-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="7f6eb-185">Specifica una proprietà di chiamata.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="7f6eb-186">[**WS \_ \_proprietà del proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span><span class="sxs-lookup"><span data-stu-id="7f6eb-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="7f6eb-187">Specifica una proprietà del proxy.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-187">Specifies a proxy property.</span></span> |



 

 

 




