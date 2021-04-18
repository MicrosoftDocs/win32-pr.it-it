---
title: Esempi di servizi Web Windows
description: Negli esempi seguenti viene illustrato come utilizzare l'API dei servizi Web Windows.
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297917"
---
# <a name="windows-web-services-examples"></a>Esempi di servizi Web Windows

Negli esempi seguenti viene illustrato come utilizzare l'API dei servizi Web Windows.

-   [Esempi di modelli di servizio](service-model-examples.md)
-   [Esempi di livello del canale TCP](tcp-channel-layer-examples.md)
-   [Esempi di livello del canale HTTP](http-channel-layer-examples.md)
-   [Esempi di livelli di canale UDP](udp-channel-layer-examples.md)
-   [Esempi di livelli di canale named pipe](named-pipes-channel-layer-examples.md)
-   [Esempi di messaggi](message-examples.md)
-   [Esempi di XML](xml-examples.md)
-   [Esempi di modelli asincroni](async-model-examples.md)
-   [Esempi di livelli di canale di sicurezza](security-channel-layer-examples.md)
-   [Esempi di replica di file](file-replication-examples.md)

## <a name="service-model-examples"></a>Esempi di modelli di servizio

Servizio calcolatrice: client: [HttpCalculatorClientExample](httpcalculatorclientexample.md), server: [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).

Servizio di calcolo con sicurezza del trasporto SSL: client: [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), server: [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).

Servizio di calcolatrice con nome utente sulla sicurezza in modalità mista SSL: client: [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), server: [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).

Servizio di calcolo con Kerberos sulla sicurezza in modalità mista SSL: client: [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), server: [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).

Servizio ordini di acquisto: client: [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), server: [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).

Servizio ordini di acquisto con sicurezza del trasporto SSL: client: [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), server: [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).

Servizio ordini di acquisto con nome utente su sicurezza in modalità mista SSL: client: [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), server: [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).

Servizio ordini di acquisto con Kerberos sulla sicurezza in modalità mista SSL: client: [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), server: [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).

Servizio di ordine di acquisto non tipizzato: Server: [UnTypedServiceExample](untypedserviceexample.md). Client: [UnTypedClientExample](untypedclientexample.md)

Calcolatore con sessione: Server: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Client:[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).

Calcolatore con un'implementazione del canale e del listener personalizzati: Server:[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md). Client:[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).

Calcolatore con un canale codificato: Server:[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md). Client:[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).

Servizio che gestisce le richieste HTTP non elaborate (non SOAP): client:[HttpRawClientExample](httprawclientexample.md). Server:[HttpRawServiceExample](httprawserviceexample.md).

Notifica di interruzione dell'operazione del servizio: Server: [BlockingServiceExample](blockingserviceexample.md). Client:[ServiceCancellationExample](servicecancellationexample.md).

Annullamento chiamata: Server: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md). Client:[CallAbandonExample](callabandonexample.md).

Creare manualmente una descrizione dei criteri e usarla per creare un proxy del servizio: [PolicyTemplateExample](policytemplateexample.md).

## <a name="tcp-channel-layer-examples"></a>Esempi di livello del canale TCP

Esempio TCP che invia messaggi usando un modello unidirezionale: client: [OneWayTcpClientExample](onewaytcpclientexample.md), server: [OneWayTcpServerExample](onewaytcpserverexample.md)

Esempio TCP che invia messaggi usando un modello Request/Reply: client: [RequestReplyTcpClientExample](requestreplytcpclientexample.md), server: [RequestReplyTcpServerExample](requestreplytcpserverexample.md)

Esempio di streaming TCP: client: [StreamingTcpClientExample](streamingtcpclientexample.md), server: [StreamingTcpServerExample](streamingtcpserverexample.md)

Esempio TCP di streaming asincrono: client: [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), server: [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)

## <a name="http-channel-layer-examples"></a>Esempi di livello del canale HTTP

Esempio HTTP: client: [HttpClientExample](httpclientexample.md), server: [HttpServerExample](httpserverexample.md)

Esempio HTTP che usa le API di streaming: client: [StreamingHttpClientExample](streaminghttpclientexample.md), server: [StreamingHttpServerExample](streaminghttpserverexample.md)

## <a name="udp-channel-layer-examples"></a>Esempi di livelli di canale UDP

Esempio UDP che invia messaggi usando un modello unidirezionale: client: [OneWayUdpClientExample](onewayudpclientexample.md), server: [OneWayUdpServerExample](onewayudpserverexample.md)

Esempio UDP che invia messaggi usando un modello di risposta di richiesta multicast: client: [MulticastUdpClientExample](multicastudpclientexample.md), server: [MulticastUdpServerExample](multicastudpserverexample.md) di seguito è riportato lo stesso esempio, ma usando l'indirizzamento IPv6: client: [MulticastUdpClientExample6](multicastudpclientexample6.md), server: [MulticastUdpServerExample6](multicastudpserverexample6.md)

## <a name="named-pipes-channel-layer-examples"></a>Esempi di livelli di canale named pipe

Esempio di named pipe che invia messaggi usando un modello Request/Reply: client: [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), server: [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)

Esempio di streaming Named Pipes: client: [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), server: [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)

## <a name="message-examples"></a>Esempi di messaggi

Esempio che usa intestazioni di messaggio personalizzate: [CustomHeaderExample](customheaderexample.md)

Esempio che codifica e decodifica un messaggio: [MessageEncodingExample](messageencodingexample.md)

Esempio che invia un messaggio: [ForwardMessageExample](forwardmessageexample.md)

## <a name="xml-examples"></a>Esempi di XML

Esempio che scrive e legge XML usando un buffer XML [ReadWriteXmlExample](readwritexmlexample.md)

Esempio che scrive e legge dati binari usando MTOM, WsWriteBytes, WsPushBytes e WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)

Esempio che consente di spostarsi in un buffer XML [NavigateXmlExample](navigatexmlexample.md)

Esempio che legge un nodo del documento XML in base al nodo [ReadXmlExample](readxmlexample.md)

Esempio che trova e visualizza un attributo XML [ReadAttributeExample](readattributeexample.md)

Esempio che scrive e legge una matrice di elementi [ReadWriteArrayExample](readwritearrayexample.md)

Esempio che inserisce un elemento in un buffer XML [InsertElementExample](insertelementexample.md)

Esempio che illustra l'uso di alcune funzioni helper del buffer XML [XmlBufferExample](xmlbufferexample.md)

Esempio che scrive e legge il tipo derivato usando le funzioni di supporto generate da WSUTIL [DerivedTypeExample](derivedtypeexample.md)

## <a name="async-model-examples"></a>Esempi di modelli asincroni

Esempio che illustra il modello per le funzioni asincrone. [AsyncModelExample](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a>Esempi di livelli di canale di sicurezza

Sicurezza del trasporto Windows su TCP: client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Sicurezza del trasporto Windows su Named Pipes: client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Sicurezza del trasporto SSL: client: [HttpClientWithSslExample](httpclientwithsslexample.md), server: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nome utente sulla sicurezza in modalità mista SSL: client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nome utente sulla sicurezza in modalità mista SSL: client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

## <a name="metadata-example"></a>Esempio di metadati

Gli esempi seguenti illustrano come elaborare documenti WSDL e dei criteri con l'obiettivo di estrarre informazioni sul protocollo supportato da un endpoint.

Nome utente sulla sicurezza in modalità mista SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emesso sulla sicurezza in modalità mista SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificato X509 sulla sicurezza in modalità mista SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="ws-metadata-exchange-example"></a>Esempio di WS-Metadata Exchange

Negli esempi seguenti viene illustrato come abilitare WS-MetadataExchange sull' [ \_ \_ host WS Service](ws-service-host.md).

Servizio TCP con WS-MetadataExchange abilitato: [MetadataExchangeSample](metadataexchangesample.md). Client moniker servizio WCF che effettua chiamate nel servizio TCP con WS-MetadataExchange abilitato: [ServiceMonikerSample](servicemonikersample.md).

## <a name="custom-headers-and-service-model"></a>Intestazioni personalizzate e modello di servizio

Negli esempi seguenti viene illustrato come utilizzare rispettivamente le intestazioni personalizzate con [WS \_ Service \_ proxy](ws-service-proxy.md) e [WS \_ Service \_ host](ws-service-host.md) .

Client: [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), server: [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).

## <a name="file-replication-sample"></a>Esempio di replica file

Un esempio completo che illustra come implementare un servizio Replica file: strumento: [FileRepToolExample](filereptoolexample.md), servizio: [FileRepServiceExample](filerepserviceexample.md).

## <a name="wcf-public-service-interoperation"></a>Interoperatività servizio pubblico WCF

Un client di servizi Web Windows comunica con un client del servizio WCF: [WcfPublicServiceSample](wcfpublicservicesample.md).

## <a name="custom-http-proxy"></a>Proxy HTTP personalizzato

Un client di servizi Web Windows comunica con un servizio TerraService ASMX utilizzando un client proxy personalizzato: [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)

 

 




