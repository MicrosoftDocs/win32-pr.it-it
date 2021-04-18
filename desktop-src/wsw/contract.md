---
title: Contratto
description: Un contratto di servizio contiene metadati che definiscono la modalità di gestione dei messaggi del canale da parte di un servizio.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Servizi Web di contratto per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120346dac4d11c21955cd2430ed0a7dc277e88c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104558963"
---
# <a name="contract"></a>Contratto

Un contratto di servizio contiene metadati che definiscono la modalità di gestione dei messaggi del canale da parte di un servizio.


Un [**\_ \_ contratto di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) trasporta metadati per un servizio per la gestione di un [ \_ messaggio WS](ws-message.md).

![Diagramma che mostra i metadati di WS_SERVICE_CONTRACT in un messaggio a un endpoint del servizio.](images/servicecontractintro.png)

Include una [**Descrizione del \_ contratto \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) e una tabella di funzioni. Un'applicazione può facoltativamente specificare [**il \_ \_ callback di \_ ricezione \_ del messaggio WS Service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Se non viene fornita una [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) e una tabella di funzioni, l'applicazione deve specificare [**il \_ \_ callback di \_ ricezione \_ del messaggio WS Service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagramma che mostra le operazioni di aggiunta e sottrazione del servizio nel contratto di servizio ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Per informazioni dettagliate, vedere l'esempio di [calcolatrice](httpcalculatorserviceexample.md) .

Descrizione del contratto

[**WS \_ La \_ Descrizione del contratto**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) è costituita dai metadati che definiscono il tipo di contratto del servizio. Generato dal [wsutil.exe](web-service-compiler-tool.md).

In termini di WSDL, una [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) esegue il mapping a un elemento WSDL: PortType. Per ogni elemento WSDL: portType nel documento WSDL viene generata **una \_ \_ Descrizione del contratto WS** distinta.

Una descrizione del contratto è costituita da una o più [operazioni del servizio](service-operation.md). Queste operazioni vengono fornite come una matrice di [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagramma che mostra un WS_CONTRACT_DESCRIPTION come una matrice di WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

``` syntax
<wsdl:definitions xmlns:soap="https://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="https://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="https://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="https://Example.org" 
xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="https://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="https://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="https://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="https://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="https://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="https://www.w3.org/2005/08/addressing" 
xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="https://Example.org" 
xmlns:wsdl="https://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="https://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="https://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

Per informazioni dettagliate su WSDL: portType per la conversione della [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) , vedere la [sezione output WSDL](wsdl-support.md).

Esempio: [ **\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Tabella Function

La tabella Function è uno struct di puntatori a funzione che rappresentano ogni [operazione del servizio](service-operation.md) nel contratto di servizio. La definizione della tabella Function viene generata anche da [wsutil.exe](web-service-compiler-tool.md).

Esempio: tabella Function

``` syntax
 // Function Table
struct CalculatorServiceFunctionTable
{
      AddOperation Add;
      SubtractOperation Subtract;
};

// Populate the Function Table
static const CalculatorServiceFunctionTable calculatorFunctions = {Add, Subtract};
```

Utilizzo del [ **\_ callback di \_ \_ ricezione del \_ messaggio WS Service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ Il \_ \_ \_ callback di ricezione del messaggio di servizio**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) ha un ruolo doppio che si escludono a vicenda.

Se per il [**\_ \_ contratto di servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)viene specificata una [**\_ \_ Descrizione del contratto WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) , questo diventa il gestore di messaggi predefinito per tutte le azioni che non sono supportate dalla **\_ \_ Descrizione del contratto WS** specificata. In caso contrario, se la **\_ \_ Descrizione del contratto WS** non è specificata nel **\_ \_ contratto di servizio WS** e il callback di ricezione del [**\_ \_ messaggio \_ \_ WS Service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) viene specificato nel **contratto di \_ servizio \_ WS** , tutti i [messaggi](ws-message.md) in arrivo vengono passati al callback.

Per altri esempi, vedere

-   [Esempio di servizio non tipizzato](untypedserviceexample.md)
-   [Esempio di servizio calcolatrice](httpcalculatorserviceexample.md)
-   [Operazioni del servizio](service-operation.md)

I callback seguenti fanno parte del contratto:

-   [**\_ \_ \_ callback ricezione messaggio servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_ \_ callback Stub servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Le strutture seguenti fanno parte del contratto:

-   [**\_Descrizione contratto \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**\_contratto del servizio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




