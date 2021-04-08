---
title: Importazione di metadati
description: Il WWSAPI include elementi API che possono essere usati per elaborare WSDL e criteri da un endpoint con l'obiettivo di estrarre informazioni che possono essere usate per comunicare con l'endpoint.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Servizi Web per l'importazione di metadati per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734991"
---
# <a name="metadata-import"></a><span data-ttu-id="4079a-106">Importazione di metadati</span><span class="sxs-lookup"><span data-stu-id="4079a-106">Metadata Import</span></span>

<span data-ttu-id="4079a-107">Il WWSAPI include elementi API che possono essere usati per elaborare WSDL e criteri da un endpoint con l'obiettivo di estrarre informazioni che possono essere usate per comunicare con l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4079a-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="4079a-108">Queste API vengono in genere usate quando il protocollo di comunicazione supportato dall'endpoint non è già noto.</span><span class="sxs-lookup"><span data-stu-id="4079a-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="4079a-109">Usare la sequenza seguente per elaborare i metadati:</span><span class="sxs-lookup"><span data-stu-id="4079a-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="4079a-110">per informazioni sul modo in cui le asserzioni WSDL e WS-Policy corrispondono all'API, vedere l'argomento [mapping dei metadati](metadata-mapping.md) .</span><span class="sxs-lookup"><span data-stu-id="4079a-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="4079a-111">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="4079a-111">Security</span></span>

<span data-ttu-id="4079a-112">I metadati scaricati sono validi solo per l'indirizzo usato per scaricarlo.</span><span class="sxs-lookup"><span data-stu-id="4079a-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="4079a-113">Un'applicazione deve assicurarsi che sia attendibile per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="4079a-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="4079a-114">Inoltre, un'applicazione deve assicurarsi che usi un protocollo di sicurezza per scaricare i documenti di metadati che non consentono la manomissione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="4079a-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="4079a-115">Un'applicazione deve ispezionare gli indirizzi dei servizi esposti dai metadati.</span><span class="sxs-lookup"><span data-stu-id="4079a-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="4079a-116">Per impostazione predefinita, il runtime garantisce che il nome host del servizio corrisponda a quello dell'URL originale usato per scaricare i metadati, ma l'applicazione potrebbe voler eseguire ulteriori controlli.</span><span class="sxs-lookup"><span data-stu-id="4079a-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="4079a-117">Un'applicazione può disabilitare la verifica del nome host sovrascrivendo la proprietà di [**\_ Verifica dei \_ \_ \_ \_ nomi host della proprietà WS Metadata**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) .</span><span class="sxs-lookup"><span data-stu-id="4079a-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="4079a-118">Se il controllo hostname eseguito per impostazione predefinita è disabilitato, l'applicazione dovrà proteggersi dai documenti dei metadati che contengono l'indirizzo di un servizio di un'entità diversa che non considera attendibile in altro modo.</span><span class="sxs-lookup"><span data-stu-id="4079a-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="4079a-119">Per impostazione predefinita, la quantità massima di memoria usata dal runtime dei metadati per deserializzare ed elaborare i metadati è 256K e il numero massimo di documenti che è possibile aggiungere è 32.</span><span class="sxs-lookup"><span data-stu-id="4079a-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="4079a-120">Questi valori predefiniti possono essere sovrascritti dalle proprietà delle [**\_ \_ \_ \_ \_ dimensioni richieste dell'heap delle proprietà dei metadati WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) e dalle proprietà **\_ dei metadati WS \_ \_ Max \_ Documents** .</span><span class="sxs-lookup"><span data-stu-id="4079a-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="4079a-121">Questi limiti sono progettati per limitare la quantità di download e limitare la quantità di memoria allocata per accumulare i metadati.</span><span class="sxs-lookup"><span data-stu-id="4079a-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="4079a-122">L'aumento di questi valori può causare un utilizzo eccessivo della memoria, l'utilizzo della CPU o la larghezza di banda di rete.</span><span class="sxs-lookup"><span data-stu-id="4079a-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="4079a-123">Si noti che, a causa dell'espansione delle stringhe del dizionario nel formato binario, un piccolo messaggio può causare un formato deserializzato molto più grande, quindi basarsi su messaggi di piccole dimensioni per limitare l'allocazione di memoria dei metadati non è sufficiente quando si usa il formato binario.</span><span class="sxs-lookup"><span data-stu-id="4079a-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="4079a-124">Per impostazione predefinita, il numero massimo di alternative dei criteri è 32, anche se può essere sovrascritto dalla proprietà della [**\_ \_ proprietà \_ Max \_ alternative della proprietà dei criteri WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) .</span><span class="sxs-lookup"><span data-stu-id="4079a-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="4079a-125">Se un'applicazione esegue il ciclo di ogni alternativa cercando una corrispondenza, potrebbe essere necessario eseguire una ricerca in tutte le alternative prima di trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="4079a-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="4079a-126">L'aumento del numero massimo di alternative può causare un utilizzo eccessivo della CPU.</span><span class="sxs-lookup"><span data-stu-id="4079a-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="4079a-127">Le enumerazioni seguenti fanno parte dell'importazione dei metadati:</span><span class="sxs-lookup"><span data-stu-id="4079a-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="4079a-128">**\_ID della \_ proprietà dei metadati WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="4079a-129">**\_stato metadati \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4079a-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="4079a-130">**\_tipo di \_ estensione \_ criteri WS**</span><span class="sxs-lookup"><span data-stu-id="4079a-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="4079a-131">**\_ID della \_ proprietà dei criteri WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="4079a-132">**\_stato criteri \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4079a-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="4079a-133">**\_tipo di \_ vincolo di associazione di sicurezza WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="4079a-134">Le funzioni seguenti fanno parte dell'importazione dei metadati:</span><span class="sxs-lookup"><span data-stu-id="4079a-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="4079a-135">**WsCreateMetadata**</span><span class="sxs-lookup"><span data-stu-id="4079a-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="4079a-136">**WsFreeMetadata**</span><span class="sxs-lookup"><span data-stu-id="4079a-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="4079a-137">**WsGetMetadataEndpoints**</span><span class="sxs-lookup"><span data-stu-id="4079a-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="4079a-138">**WsGetMetadataProperty**</span><span class="sxs-lookup"><span data-stu-id="4079a-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="4079a-139">**WsGetMissingMetadataDocumentAddress**</span><span class="sxs-lookup"><span data-stu-id="4079a-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="4079a-140">**WsGetPolicyAlternativeCount**</span><span class="sxs-lookup"><span data-stu-id="4079a-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="4079a-141">**WsGetPolicyProperty**</span><span class="sxs-lookup"><span data-stu-id="4079a-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="4079a-142">**WsMatchPolicyAlternative**</span><span class="sxs-lookup"><span data-stu-id="4079a-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="4079a-143">**WsReadMetadata**</span><span class="sxs-lookup"><span data-stu-id="4079a-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="4079a-144">**WsResetMetadata**</span><span class="sxs-lookup"><span data-stu-id="4079a-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="4079a-145">Gli handle seguenti fanno parte dell'importazione dei metadati:</span><span class="sxs-lookup"><span data-stu-id="4079a-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="4079a-146">\_metadati WS</span><span class="sxs-lookup"><span data-stu-id="4079a-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="4079a-147">\_criteri WS</span><span class="sxs-lookup"><span data-stu-id="4079a-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="4079a-148">Le strutture seguenti fanno parte dell'importazione dei metadati:</span><span class="sxs-lookup"><span data-stu-id="4079a-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="4079a-149">**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="4079a-150">**\_vincolo della \_ proprietà del canale WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="4079a-151">**\_ \_ estensione criteri WS \_ endpoint**</span><span class="sxs-lookup"><span data-stu-id="4079a-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="4079a-152">**\_vincolo di \_ \_ binding di \_ sicurezza \_ \_ per l'autenticazione dell'intestazione WS http**</span><span class="sxs-lookup"><span data-stu-id="4079a-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="4079a-153">**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="4079a-154">**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="4079a-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="4079a-155">**\_endpoint dei metadati WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="4079a-156">**\_endpoint dei metadati WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="4079a-157">**\_Proprietà metadati \_ WS**</span><span class="sxs-lookup"><span data-stu-id="4079a-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="4079a-158">**\_vincoli dei criteri WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="4079a-159">**\_estensione dei criteri WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="4079a-160">**\_proprietà dei criteri WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="4079a-161">**\_proprietà dei criteri WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="4079a-162">**\_vincolo della \_ \_ Proprietà token \_ di sicurezza WS Request \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="4079a-163">**\_vincolo di \_ associazione di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="4079a-164">**\_vincolo della \_ proprietà di associazione di sicurezza WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="4079a-165">**\_vincoli di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="4079a-166">**\_vincolo di \_ \_ associazione di sicurezza del messaggio del contesto \_ di \_ sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="4079a-167">**\_vincolo della \_ proprietà di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="4079a-168">**\_vincolo di \_ binding di sicurezza del trasporto \_ \_ di WS SSL \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="4079a-169">**\_vincolo di \_ \_ binding di sicurezza del trasporto SSPI \_ \_ di WS TCP \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="4079a-170">**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4079a-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




