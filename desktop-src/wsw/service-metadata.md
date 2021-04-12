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
# <a name="service-metadata"></a>Metadati del servizio

L'host del servizio WWSAPI supporta WS-MetadataExchange per gli endpoint. Per abilitare lo scambio di metadati nell'host del servizio, attenersi alla procedura seguente:

-   Specificare i documenti di metadati nella proprietà [**WS \_ Service \_ Metadata**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) nell' [ \_ \_ host WS Service](ws-service-host.md).
-   Specificare il nome del servizio nella [**proprietà \_ \_ metadati del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) nell' [ \_ \_ host del servizio WS](ws-service-host.md).
-   Specificare la porta per i singoli endpoint utilizzando la proprietà [**\_ metadati della \_ \_ proprietà dell' \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) nell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).
-   Abilitare una o più strutture dell' [**\_ \_ endpoint WS Service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) per soddisfare le richieste di WS-MetadataExchange.
-   Facoltativamente, specificare **il \_ \_ \_ \_ \_ \_ \_ suffisso URL di scambio dei metadati della proprietà dell'endpoint di servizio WS** nell'enumerazione dell' [**\_ \_ \_ \_ ID di proprietà dell'endpoint del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) per la manutenzione Ws-MetadataExchange richieste su un indirizzo specifico.


Impostazione del nome del servizio/documenti di metadati nell'host del servizio

Il primo passaggio consiste nel specificare i documenti dei metadati nell'host del servizio. A tale scopo, raccogliere i singoli documenti come una matrice di \_ stringhe WS-XML \_ \* . Queste stringhe possono essere XML Schema, WSDL o WS-Policy documento. Viene specificato tramite la proprietà [**\_ \_ \_ dei metadati della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .

Facoltativamente, un'applicazione può inoltre specificare il nome e lo spazio dei nomi del servizio come parte dei [**\_ \_ metadati del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata). Se il documento di metadati non specifica l'elemento Service per il nome del servizio specificato, il modello di servizio genererà un elemento Service con le porte WSDL corrispondenti per il servizio.

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

Si noti che non verrà eseguita alcuna verifica dei singoli documenti di metadati sui documenti. È responsabilità dell'applicazione convalidare il contenuto dei documenti e assicurarsi che tutti i percorsi di importazione siano relativamente specificati.

Lo spazio dei nomi specificato viene utilizzato per individuare il documento in cui l'elemento del servizio verrà aggiunto dall'host del servizio.

Aggiunta dell'elemento Service al documento WSDL

L'host del servizio fornisce funzionalità che consentono all'applicazione di aggiungere un elemento di servizio per suo conto, se non ne è già stato specificato uno. Per abilitare questo comportamento, un'applicazione deve specificare i campi serivceName e serviceNs nella struttura [**\_ \_ dei metadati del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) . Se ServiceName e serviceNs sono entrambi **null** , nessun elemento servizio viene aggiunto al documento WSDL. Entrambi questi vengono usati per identificare il documento in cui verrà aggiunto l'oggetto ServiceElement.

Se la proprietà [**\_ \_ \_ dei metadati della proprietà WS Service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) non è specificata, non verrà eseguita alcuna Exchange dei metadati nell'host del servizio.

Specifica della porta nell'endpoint del \_ servizio \_ WS

Affinché un [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) sia disponibile come porta all'interno dell'elemento Service nel documento WSDL, è necessario che l'applicazione specifichi la proprietà di metadati della [**proprietà dell'endpoint di \_ servizio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .

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

Si presuppone che il riferimento al nome e allo spazio dei nomi dell'associazione esista nei documenti specificati nell'host del servizio come parte dei \_ metadati della proprietà WS Service \_ \_ . Il runtime non verifica questa operazione per conto dell'applicazione.

Abilitare la manutenzione WS-MetadataExchange sull' \_ endpoint WS Service \_

Per soddisfare le richieste di WS-MetadataExchange, è necessario che nell'host del servizio sia abilitato almeno un endpoint per la manutenzione delle richieste di WS-MetadataExchange. Questa operazione viene eseguita impostando la versione appropriata per WS-MetadataExchange nell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Abilitare la manutenzione HTTP GET sull' \_ endpoint WS Service \_

Per serviceHTTP richieste GET, per l'host del servizio deve essere abilitato almeno un endpoint per la manutenzione delle richieste WS-MetadataExchange. Questa operazione viene eseguita impostando la versione appropriata per WS-MetadataExchange nell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

Specifica del suffisso URL per richieste di Ws-MetadataExchange

Un'applicazione può facoltativamente abilitare solo l'accettazione delle richieste per WS-MetadataExchange in un percorso specifico. Questa operazione viene eseguita specificando un suffisso per l' \_ endpoint di servizio WS specificato \_ . Questo suffisso è concatenato così com'è all'URL effettivo per l' \_ endpoint del servizio WS \_ . La stringa concatenata viene utilizzata come URL corrispondente all'intestazione ' to ' ricevuta.

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

Gli elementi API seguenti sono correlati al servizio metadati.

| Enumerazione                                                       | Descrizione                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_tipo di \_ scambio \_ metadati WS**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | Abilita o Disabilita WS-MetadataExchange e la manutenzione HTTP GET sull'endpoint. |



 



| Struttura                                                               | Descrizione                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_metadati dell' \_ endpoint del servizio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | Rappresenta l'elemento porta per l'endpoint.                         |
| [**\_metadati del servizio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | Specifica la matrice di documenti dei metadati del servizio.                       |
| [**\_ \_ documento metadati del servizio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | Specifica i singoli documenti che costituiscono i metadati del servizio. |



 

 

 




