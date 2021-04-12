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
# <a name="service-model-layer-overview"></a><span data-ttu-id="802cb-106">Panoramica del livello del modello di servizio</span><span class="sxs-lookup"><span data-stu-id="802cb-106">Service Model Layer Overview</span></span>

<span data-ttu-id="802cb-107">L'API del modello del servizio WWSAPI modella la comunicazione tra un client e un servizio come chiamate al metodo, anziché come messaggi di dati.</span><span class="sxs-lookup"><span data-stu-id="802cb-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="802cb-108">A differenza del [livello del canale](channel-layer-overview.md), che supporta scambi di [messaggi](message.md) più tradizionali tra client e servizio, il modello di servizio gestisce automaticamente la comunicazione per mezzo di un proxy del servizio nel client e in un host del servizio nel servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="802cb-109">Ciò significa che il client chiama le funzioni generate e il server implementa i callback.</span><span class="sxs-lookup"><span data-stu-id="802cb-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="802cb-110">Si consideri, ad esempio, un servizio di calcolatrice che esegue addizioni e sottrazioni su due numeri.</span><span class="sxs-lookup"><span data-stu-id="802cb-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="802cb-111">L'addizione e la sottrazione sono operazioni naturalmente rappresentate come chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="802cb-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![Diagramma che illustra il modo in cui un servizio di calcolatrice comunica con un client usando le chiamate al metodo per l'addizione e la sottrazione.](images/servicemodelintro.png)

<span data-ttu-id="802cb-113">Il modello di servizio rappresenta la comunicazione tra il client e il servizio come chiamate al metodo dichiarate, quindi nasconde i dettagli di comunicazione del livello del canale sottostante dall'applicazione, semplificando l'implementazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="802cb-114">Specifica di un servizio</span><span class="sxs-lookup"><span data-stu-id="802cb-114">Specifying a Service</span></span>

<span data-ttu-id="802cb-115">È necessario specificare un servizio in termini di modelli di scambio dei messaggi, nonché della relativa rappresentazione dei dati di rete.</span><span class="sxs-lookup"><span data-stu-id="802cb-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="802cb-116">Per i servizi, questa specifica viene in genere fornita come documento WSDL e XML Schema.</span><span class="sxs-lookup"><span data-stu-id="802cb-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="802cb-117">Il documento WSDL è un documento XML che contiene l'associazione di canale e i modelli di scambio dei messaggi del servizio, mentre il documento XML Schema è un documento XML che definisce la rappresentazione dei dati dei singoli messaggi.</span><span class="sxs-lookup"><span data-stu-id="802cb-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="802cb-118">Per il servizio di calcolatrice e per le operazioni di addizione e sottrazione, il documento WSDL potrebbe essere simile all'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="802cb-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

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

<span data-ttu-id="802cb-119">Analogamente, il XML Schema può essere definito come segue:</span><span class="sxs-lookup"><span data-stu-id="802cb-119">Likewise, its XML schema can be defined as follows:</span></span>

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

## <a name="converting-metadata-to-code"></a><span data-ttu-id="802cb-120">Conversione di metadati nel codice</span><span class="sxs-lookup"><span data-stu-id="802cb-120">Converting Metadata to Code</span></span>

<span data-ttu-id="802cb-121">Il modello di servizio fornisce il [WsUtil.exe](web-service-compiler-tool.md) come strumento per elaborare questi documenti di metadati, convertendo un file WSDL in un'intestazione C e nei file di origine.</span><span class="sxs-lookup"><span data-stu-id="802cb-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![Diagramma che illustra come WsUtil.exe converte un file WSDL in un'intestazione C e nei file di origine.](images/doctotool.png)

<span data-ttu-id="802cb-123">Il [WsUtil.exe](web-service-compiler-tool.md) genera intestazioni e origini per l'implementazione del servizio, nonché le operazioni del servizio sul lato client per il client.</span><span class="sxs-lookup"><span data-stu-id="802cb-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="802cb-124">Chiamata del servizio di calcolatrice da un client</span><span class="sxs-lookup"><span data-stu-id="802cb-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="802cb-125">Come per l'implementazione del servizio, il client deve includere l'intestazione o le intestazioni generate.</span><span class="sxs-lookup"><span data-stu-id="802cb-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="802cb-126">A questo punto, l'applicazione client può creare e aprire un proxy del servizio per iniziare la comunicazione con il servizio calcolatrice.</span><span class="sxs-lookup"><span data-stu-id="802cb-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="802cb-127">L'applicazione può chiamare l'operazione di aggiunta sul servizio di calcolatrice con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="802cb-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="802cb-128">Per un'implementazione completa del servizio di calcolatrice, fare riferimento all'esempio di codice in [HttpCalculatorClientExample](httpcalculatorclientexample.md) .</span><span class="sxs-lookup"><span data-stu-id="802cb-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="802cb-129">Componenti del modello di servizio</span><span class="sxs-lookup"><span data-stu-id="802cb-129">Service Model Components</span></span>

<span data-ttu-id="802cb-130">L'interazione dei singoli componenti del modello di servizio WWSAPI nell'esempio di calcolatrice è la seguente:</span><span class="sxs-lookup"><span data-stu-id="802cb-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="802cb-131">Il client crea un [proxy del servizio](service-proxy.md) e lo apre.</span><span class="sxs-lookup"><span data-stu-id="802cb-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="802cb-132">Il client chiama la funzione Add del servizio e passa il proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="802cb-133">Il messaggio viene serializzato in base ai metadati di serializzazione nell'intestazione e nei file di origine generati dallo strumento metadati ([WsUtil.exe](web-service-compiler-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="802cb-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="802cb-134">Il messaggio viene scritto nel canale e trasmesso attraverso la rete al servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="802cb-135">Sul lato server, il servizio è ospitato all'interno di un host del servizio e dispone di un endpoint in ascolto per il contratto ICalculator.</span><span class="sxs-lookup"><span data-stu-id="802cb-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="802cb-136">Utilizzando i metadati del modello di servizio nello stub, il servizio deserializza il messaggio dal client e lo invia allo stub.</span><span class="sxs-lookup"><span data-stu-id="802cb-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="802cb-137">Il servizio lato server chiama il metodo Add e lo passa al contesto dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="802cb-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="802cb-138">Questo contesto dell'operazione contiene il riferimento al messaggio in ingresso.</span><span class="sxs-lookup"><span data-stu-id="802cb-138">This operation context contains the reference to the incoming message.</span></span>

![Diagramma che illustra l'interazione dei singoli componenti del modello del servizio WWSAPI.](images/servicemodellayout.png)

<span data-ttu-id="802cb-140">Componenti</span><span class="sxs-lookup"><span data-stu-id="802cb-140">Components</span></span>

-   <span data-ttu-id="802cb-141">[Host del servizio](service-host.md): ospita un servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="802cb-142">[Proxy del servizio](service-proxy.md): definisce il modo in cui un client comunica con un servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="802cb-143">[Context](context.md): contenitore delle proprietà per rendere disponibili informazioni specifiche dello stato per un'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="802cb-144">[Contract](contract.md): definizione dell'interfaccia di un servizio.</span><span class="sxs-lookup"><span data-stu-id="802cb-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="802cb-145">Ad esempio, ICalculator rappresenta un contratto per il servizio di calcolatrice nel codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="802cb-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="802cb-146">[WsUtil.exe](web-service-compiler-tool.md): strumento di metadati del modello di servizio per la generazione di proxy e stub.</span><span class="sxs-lookup"><span data-stu-id="802cb-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




