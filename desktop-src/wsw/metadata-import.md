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
# <a name="metadata-import"></a>Importazione di metadati

Il WWSAPI include elementi API che possono essere usati per elaborare WSDL e criteri da un endpoint con l'obiettivo di estrarre informazioni che possono essere usate per comunicare con l'endpoint. Queste API vengono in genere usate quando il protocollo di comunicazione supportato dall'endpoint non è già noto.


Usare la sequenza seguente per elaborare i metadati:

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

per informazioni sul modo in cui le asserzioni WSDL e WS-Policy corrispondono all'API, vedere l'argomento [mapping dei metadati](metadata-mapping.md) .

## <a name="security"></a>Sicurezza

I metadati scaricati sono validi solo per l'indirizzo usato per scaricarlo. Un'applicazione deve assicurarsi che sia attendibile per l'indirizzo. Inoltre, un'applicazione deve assicurarsi che usi un protocollo di sicurezza per scaricare i documenti di metadati che non consentono la manomissione dei metadati.

Un'applicazione deve ispezionare gli indirizzi dei servizi esposti dai metadati. Per impostazione predefinita, il runtime garantisce che il nome host del servizio corrisponda a quello dell'URL originale usato per scaricare i metadati, ma l'applicazione potrebbe voler eseguire ulteriori controlli. Un'applicazione può disabilitare la verifica del nome host sovrascrivendo la proprietà di [**\_ Verifica dei \_ \_ \_ \_ nomi host della proprietà WS Metadata**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) . Se il controllo hostname eseguito per impostazione predefinita è disabilitato, l'applicazione dovrà proteggersi dai documenti dei metadati che contengono l'indirizzo di un servizio di un'entità diversa che non considera attendibile in altro modo.

Per impostazione predefinita, la quantità massima di memoria usata dal runtime dei metadati per deserializzare ed elaborare i metadati è 256K e il numero massimo di documenti che è possibile aggiungere è 32. Questi valori predefiniti possono essere sovrascritti dalle proprietà delle [**\_ \_ \_ \_ \_ dimensioni richieste dell'heap delle proprietà dei metadati WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) e dalle proprietà **\_ dei metadati WS \_ \_ Max \_ Documents** . Questi limiti sono progettati per limitare la quantità di download e limitare la quantità di memoria allocata per accumulare i metadati. L'aumento di questi valori può causare un utilizzo eccessivo della memoria, l'utilizzo della CPU o la larghezza di banda di rete. Si noti che, a causa dell'espansione delle stringhe del dizionario nel formato binario, un piccolo messaggio può causare un formato deserializzato molto più grande, quindi basarsi su messaggi di piccole dimensioni per limitare l'allocazione di memoria dei metadati non è sufficiente quando si usa il formato binario.

Per impostazione predefinita, il numero massimo di alternative dei criteri è 32, anche se può essere sovrascritto dalla proprietà della [**\_ \_ proprietà \_ Max \_ alternative della proprietà dei criteri WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) . Se un'applicazione esegue il ciclo di ogni alternativa cercando una corrispondenza, potrebbe essere necessario eseguire una ricerca in tutte le alternative prima di trovare una corrispondenza. L'aumento del numero massimo di alternative può causare un utilizzo eccessivo della CPU.

Le enumerazioni seguenti fanno parte dell'importazione dei metadati:

-   [**\_ID della \_ proprietà dei metadati WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**\_stato metadati \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**\_tipo di \_ estensione \_ criteri WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**\_ID della \_ proprietà dei criteri WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**\_stato criteri \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**\_tipo di \_ vincolo di associazione di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

Le funzioni seguenti fanno parte dell'importazione dei metadati:

-   [**WsCreateMetadata**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**WsFreeMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**WsGetMetadataEndpoints**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**WsGetMetadataProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**WsGetMissingMetadataDocumentAddress**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**WsGetPolicyAlternativeCount**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**WsGetPolicyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**WsMatchPolicyAlternative**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**WsReadMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**WsResetMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

Gli handle seguenti fanno parte dell'importazione dei metadati:

-   [\_metadati WS](ws-metadata.md)
-   [\_criteri WS](ws-policy.md)

Le strutture seguenti fanno parte dell'importazione dei metadati:

-   [**\_vincolo di \_ binding di sicurezza del messaggio WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_vincolo della \_ proprietà del canale WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**\_ \_ estensione criteri WS \_ endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**\_vincolo di \_ \_ binding di \_ sicurezza \_ \_ per l'autenticazione dell'intestazione WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**\_vincolo di \_ \_ associazione di sicurezza del messaggio del token \_ WS \_ emesso \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**\_vincolo di \_ \_ binding di \_ sicurezza del messaggio \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_endpoint dei metadati WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**\_endpoint dei metadati WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**\_Proprietà metadati \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**\_vincoli dei criteri WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**\_estensione dei criteri WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**\_proprietà dei criteri WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**\_proprietà dei criteri WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**\_vincolo della \_ \_ Proprietà token \_ di sicurezza WS Request \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**\_vincolo di \_ associazione di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**\_vincolo della \_ proprietà di associazione di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**\_vincoli di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**\_vincolo di \_ \_ associazione di sicurezza del messaggio del contesto \_ di \_ sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**\_vincolo della \_ proprietà di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**\_vincolo di \_ binding di sicurezza del trasporto \_ \_ di WS SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**\_vincolo di \_ \_ binding di sicurezza del trasporto SSPI \_ \_ di WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**\_vincolo di \_ binding di sicurezza del messaggio WS nomeutente \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




