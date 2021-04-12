---
title: Panoramica del livello del modello di servizio
description: L'API del modello del servizio WWSAPI modella la comunicazione tra un client e un servizio come chiamate al metodo, anziché come messaggi di dati.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Panoramica del livello del modello di servizio servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104351116"
---
# <a name="service-model-layer-overview"></a>Panoramica del livello del modello di servizio

L'API del modello del servizio WWSAPI modella la comunicazione tra un client e un servizio come chiamate al metodo, anziché come messaggi di dati. A differenza del [livello del canale](channel-layer-overview.md), che supporta scambi di [messaggi](message.md) più tradizionali tra client e servizio, il modello di servizio gestisce automaticamente la comunicazione per mezzo di un proxy del servizio nel client e in un host del servizio nel servizio. Ciò significa che il client chiama le funzioni generate e il server implementa i callback.


Si consideri, ad esempio, un servizio di calcolatrice che esegue addizioni e sottrazioni su due numeri. L'addizione e la sottrazione sono operazioni naturalmente rappresentate come chiamate al metodo.

![Diagramma che illustra il modo in cui un servizio di calcolatrice comunica con un client usando le chiamate al metodo per l'addizione e la sottrazione.](images/servicemodelintro.png)

Il modello di servizio rappresenta la comunicazione tra il client e il servizio come chiamate al metodo dichiarate, quindi nasconde i dettagli di comunicazione del livello del canale sottostante dall'applicazione, semplificando l'implementazione del servizio.

## <a name="specifying-a-service"></a>Specifica di un servizio

È necessario specificare un servizio in termini di modelli di scambio dei messaggi, nonché della relativa rappresentazione dei dati di rete. Per i servizi, questa specifica viene in genere fornita come documento WSDL e XML Schema.

Il documento WSDL è un documento XML che contiene l'associazione di canale e i modelli di scambio dei messaggi del servizio, mentre il documento XML Schema è un documento XML che definisce la rappresentazione dei dati dei singoli messaggi.

Per il servizio di calcolatrice e per le operazioni di addizione e sottrazione, il documento WSDL potrebbe essere simile all'esempio seguente:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Analogamente, il XML Schema può essere definito come segue:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a>Conversione di metadati nel codice

Il modello di servizio fornisce il [WsUtil.exe](web-service-compiler-tool.md) come strumento per elaborare questi documenti di metadati, convertendo un file WSDL in un'intestazione C e nei file di origine.

![Diagramma che illustra come WsUtil.exe converte un file WSDL in un'intestazione C e nei file di origine.](images/doctotool.png)

Il [WsUtil.exe](web-service-compiler-tool.md) genera intestazioni e origini per l'implementazione del servizio, nonché le operazioni del servizio sul lato client per il client.

## <a name="calling-the-calculator-service-from-a-client&quot;></a>Chiamata del servizio di calcolatrice da un client

Come per l'implementazione del servizio, il client deve includere l'intestazione o le intestazioni generate.

``` syntax
#include &quot;CalculatorProxyStub.h&quot;
```

A questo punto, l'applicazione client può creare e aprire un proxy del servizio per iniziare la comunicazione con il servizio calcolatrice.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L&quot;http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

L'applicazione può chiamare l'operazione di aggiunta sul servizio di calcolatrice con il codice seguente:

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

Per un'implementazione completa del servizio di calcolatrice, fare riferimento all'esempio di codice in [HttpCalculatorClientExample](httpcalculatorclientexample.md) .

## <a name="service-model-components"></a>Componenti del modello di servizio

L'interazione dei singoli componenti del modello di servizio WWSAPI nell'esempio di calcolatrice è la seguente:

-   Il client crea un [proxy del servizio](service-proxy.md) e lo apre.
-   Il client chiama la funzione Add del servizio e passa il proxy del servizio.
-   Il messaggio viene serializzato in base ai metadati di serializzazione nell'intestazione e nei file di origine generati dallo strumento metadati ([WsUtil.exe](web-service-compiler-tool.md)).
-   Il messaggio viene scritto nel canale e trasmesso attraverso la rete al servizio.
-   Sul lato server, il servizio è ospitato all'interno di un host del servizio e dispone di un endpoint in ascolto per il contratto ICalculator.
-   Utilizzando i metadati del modello di servizio nello stub, il servizio deserializza il messaggio dal client e lo invia allo stub.
-   Il servizio lato server chiama il metodo Add e lo passa al contesto dell'operazione. Questo contesto dell'operazione contiene il riferimento al messaggio in ingresso.

![Diagramma che illustra l'interazione dei singoli componenti del modello del servizio WWSAPI.](images/servicemodellayout.png)

Componenti

-   [Host del servizio](service-host.md): ospita un servizio.
-   [Proxy del servizio](service-proxy.md): definisce il modo in cui un client comunica con un servizio.
-   [Context](context.md): contenitore delle proprietà per rendere disponibili informazioni specifiche dello stato per un'operazione del servizio.
-   [Contract](contract.md): definizione dell'interfaccia di un servizio. Ad esempio, ICalculator rappresenta un contratto per il servizio di calcolatrice nel codice di esempio.
-   [WsUtil.exe](web-service-compiler-tool.md): strumento di metadati del modello di servizio per la generazione di proxy e stub.

 

 




