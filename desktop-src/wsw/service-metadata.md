---
title: Metadati del servizio
description: L'host del servizio WWSAPI supporta WS-MetadataExchange per gli endpoint.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Metadati del servizio nativi-servizi Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474678"
---
# <a name="service-metadata"></a><span data-ttu-id="d7cce-106">Metadati del servizio</span><span class="sxs-lookup"><span data-stu-id="d7cce-106">Service Metadata</span></span>

<span data-ttu-id="d7cce-107">L'host del servizio WWSAPI supporta WS-MetadataExchange per gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="d7cce-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="d7cce-108">Per abilitare lo scambio di metadati nell'host del servizio, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="d7cce-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="d7cce-109">Specificare i documenti di metadati nella proprietà [**WS \_ Service \_ Metadata**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) nell' [ \_ \_ host WS Service](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="d7cce-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="d7cce-110">Specificare il nome del servizio nella [**proprietà \_ \_ metadati del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) nell' [ \_ \_ host del servizio WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="d7cce-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="d7cce-111">Specificare la porta per i singoli endpoint utilizzando la proprietà [**\_ metadati della \_ \_ proprietà dell' \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) nell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="d7cce-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="d7cce-112">Abilitare una o più strutture dell' [**\_ \_ endpoint WS Service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) per soddisfare le richieste di WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="d7cce-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="d7cce-113">Facoltativamente, specificare **il \_ \_ \_ \_ \_ \_ \_ suffisso URL di scambio dei metadati della proprietà dell'endpoint di servizio WS** nell'enumerazione dell' [**\_ \_ \_ \_ ID di proprietà dell'endpoint del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) per la manutenzione Ws-MetadataExchange richieste su un indirizzo specifico.</span><span class="sxs-lookup"><span data-stu-id="d7cce-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="d7cce-114">Impostazione del nome del servizio/documenti di metadati nell'host del servizio</span><span class="sxs-lookup"><span data-stu-id="d7cce-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="d7cce-115">Il primo passaggio consiste nel specificare i documenti dei metadati nell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="d7cce-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="d7cce-116">A tale scopo, raccogliere i singoli documenti come una matrice di \_ stringhe WS-XML \_ \* .</span><span class="sxs-lookup"><span data-stu-id="d7cce-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="d7cce-117">Queste stringhe possono essere XML Schema, WSDL o WS-Policy documento.</span><span class="sxs-lookup"><span data-stu-id="d7cce-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="d7cce-118">Viene specificato tramite la proprietà [**\_ \_ \_ dei metadati della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="d7cce-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="d7cce-119">Facoltativamente, un'applicazione può inoltre specificare il nome e lo spazio dei nomi del servizio come parte dei [**\_ \_ metadati del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span><span class="sxs-lookup"><span data-stu-id="d7cce-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="d7cce-120">Se il documento di metadati non specifica l'elemento Service per il nome del servizio specificato, il modello di servizio genererà un elemento Service con le porte WSDL corrispondenti per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d7cce-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="d7cce-121">Si noti che non verrà eseguita alcuna verifica dei singoli documenti di metadati sui documenti.</span><span class="sxs-lookup"><span data-stu-id="d7cce-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="d7cce-122">È responsabilità dell'applicazione convalidare il contenuto dei documenti e assicurarsi che tutti i percorsi di importazione siano relativamente specificati.</span><span class="sxs-lookup"><span data-stu-id="d7cce-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="d7cce-123">Lo spazio dei nomi specificato viene utilizzato per individuare il documento in cui l'elemento del servizio verrà aggiunto dall'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="d7cce-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="d7cce-124">Aggiunta dell'elemento Service al documento WSDL</span><span class="sxs-lookup"><span data-stu-id="d7cce-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="d7cce-125">L'host del servizio fornisce funzionalità che consentono all'applicazione di aggiungere un elemento di servizio per suo conto, se non ne è già stato specificato uno.</span><span class="sxs-lookup"><span data-stu-id="d7cce-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="d7cce-126">Per abilitare questo comportamento, un'applicazione deve specificare i campi serivceName e serviceNs nella struttura [**\_ \_ dei metadati del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) .</span><span class="sxs-lookup"><span data-stu-id="d7cce-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="d7cce-127">Se ServiceName e serviceNs sono entrambi **null** , nessun elemento servizio viene aggiunto al documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="d7cce-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="d7cce-128">Entrambi questi vengono usati per identificare il documento in cui verrà aggiunto l'oggetto ServiceElement.</span><span class="sxs-lookup"><span data-stu-id="d7cce-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="d7cce-129">Se la proprietà [**\_ \_ \_ dei metadati della proprietà WS Service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) non è specificata, non verrà eseguita alcuna Exchange dei metadati nell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="d7cce-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="d7cce-130">Specifica della porta nell'endpoint del \_ servizio \_ WS</span><span class="sxs-lookup"><span data-stu-id="d7cce-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="d7cce-131">Affinché un [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) sia disponibile come porta all'interno dell'elemento Service nel documento WSDL, è necessario che l'applicazione specifichi la proprietà di metadati della [**proprietà dell'endpoint di \_ servizio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .</span><span class="sxs-lookup"><span data-stu-id="d7cce-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="d7cce-132">Si presuppone che il riferimento al nome e allo spazio dei nomi dell'associazione esista nei documenti specificati nell'host del servizio come parte dei \_ metadati della proprietà WS Service \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d7cce-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="d7cce-133">Il runtime non verifica questa operazione per conto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7cce-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="d7cce-134">Abilitare la manutenzione WS-MetadataExchange sull' \_ endpoint WS Service \_</span><span class="sxs-lookup"><span data-stu-id="d7cce-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="d7cce-135">Per soddisfare le richieste di WS-MetadataExchange, è necessario che nell'host del servizio sia abilitato almeno un endpoint per la manutenzione delle richieste di WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="d7cce-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="d7cce-136">Questa operazione viene eseguita impostando la versione appropriata per WS-MetadataExchange nell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="d7cce-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="d7cce-137">Abilitare la manutenzione HTTP GET sull' \_ endpoint WS Service \_</span><span class="sxs-lookup"><span data-stu-id="d7cce-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="d7cce-138">Per serviceHTTP richieste GET, per l'host del servizio deve essere abilitato almeno un endpoint per la manutenzione delle richieste WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="d7cce-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="d7cce-139">Questa operazione viene eseguita impostando la versione appropriata per WS-MetadataExchange nell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="d7cce-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="d7cce-140">Specifica del suffisso URL per richieste di Ws-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="d7cce-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="d7cce-141">Un'applicazione può facoltativamente abilitare solo l'accettazione delle richieste per WS-MetadataExchange in un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="d7cce-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="d7cce-142">Questa operazione viene eseguita specificando un suffisso per l' \_ endpoint di servizio WS specificato \_ .</span><span class="sxs-lookup"><span data-stu-id="d7cce-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="d7cce-143">Questo suffisso è concatenato così com'è all'URL effettivo per l' \_ endpoint del servizio WS \_ .</span><span class="sxs-lookup"><span data-stu-id="d7cce-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="d7cce-144">La stringa concatenata viene utilizzata come URL corrispondente all'intestazione ' to ' ricevuta.</span><span class="sxs-lookup"><span data-stu-id="d7cce-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="d7cce-145">Gli elementi API seguenti sono correlati al servizio metadati.</span><span class="sxs-lookup"><span data-stu-id="d7cce-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="d7cce-146">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="d7cce-146">Enumeration</span></span>                                                       | <span data-ttu-id="d7cce-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7cce-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d7cce-148">**\_tipo di \_ scambio \_ metadati WS**</span><span class="sxs-lookup"><span data-stu-id="d7cce-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="d7cce-149">Abilita o Disabilita WS-MetadataExchange e la manutenzione HTTP GET sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d7cce-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="d7cce-150">Struttura</span><span class="sxs-lookup"><span data-stu-id="d7cce-150">Structure</span></span>                                                               | <span data-ttu-id="d7cce-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7cce-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d7cce-152">**\_metadati dell' \_ endpoint del servizio WS \_**</span><span class="sxs-lookup"><span data-stu-id="d7cce-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="d7cce-153">Rappresenta l'elemento porta per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d7cce-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="d7cce-154">**\_metadati del servizio WS \_**</span><span class="sxs-lookup"><span data-stu-id="d7cce-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="d7cce-155">Specifica la matrice di documenti dei metadati del servizio.</span><span class="sxs-lookup"><span data-stu-id="d7cce-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="d7cce-156">**\_ \_ documento metadati del servizio WS \_**</span><span class="sxs-lookup"><span data-stu-id="d7cce-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="d7cce-157">Specifica i singoli documenti che costituiscono i metadati del servizio.</span><span class="sxs-lookup"><span data-stu-id="d7cce-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




