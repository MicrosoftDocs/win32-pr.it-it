---
title: Contratto
description: Un contratto di servizio contiene metadati che definiscono il modo in cui un servizio gestisce i messaggi del canale.
ms.assetid: 670530bf-344b-4480-8357-8984d80c0c68
keywords:
- Contratti di servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69be302ace90c82b7b0db5666289cf4d312458e7283a04e2a1d892faa894ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026581"
---
# <a name="contract"></a>Contratto

Un contratto di servizio contiene metadati che definiscono il modo in cui un servizio gestisce i messaggi del canale.


Un [**contratto WS \_ SERVICE \_ trasporta**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) i metadati per un servizio per gestire un [messaggio \_ WS.](ws-message.md)

![Diagramma che mostra WS_SERVICE_CONTRACT metadati in un messaggio a un endpoint di servizio.](images/servicecontractintro.png)

Include una [**WS \_ CONTRACT DESCRIPTION \_ e**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) una tabella di funzioni. Un'applicazione può specificare facoltativamente [**WS \_ SERVICE MESSAGE RECEIVE \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

Se non [**vengono specificati WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) e una tabella di funzioni, l'applicazione deve specificare [**WS SERVICE MESSAGE RECEIVE \_ \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback).

![Diagramma che illustra le operazioni del servizio Add e Subtract nel contratto di servizio ICalculator.](images/servicecontract.png)


``` syntax
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, 
    NULL, 
    &calculatorFunctions, 
};
```

Per informazioni [dettagliate, vedere](httpcalculatorserviceexample.md) l'esempio della calcolatrice.

Descrizione del contratto

[**WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) è un metadati che definisce il contratto di tipo del servizio. Generato da [wsutil.exe](web-service-compiler-tool.md).

In termini di WSDL, [**WS \_ CONTRACT DESCRIPTION esegue \_ il**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) mapping a wsdl:portType. Per ogni wsdl:portType nel documento WSDL verrà generata una **\_ \_ DESCRIZIONE WS CONTRACT** separata.

Una descrizione del contratto è costituito da una o più operazioni [del servizio](service-operation.md). Queste operazioni vengono fornite come matrice di [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description).

![Diagramma che mostra un WS_CONTRACT_DESCRIPTION come matrice di WS_OPERATION_DESCRIPTIONs.](images/porttypetocontract.png)

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

Per informazioni dettagliate sulla conversione da wsdl:portType [**a WS \_ CONTRACT \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) vedere la [sezione relativa all'output WSDL](wsdl-support.md).

Esempio: [ **WS \_ CONTRACT \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)

``` syntax
static WS_CONTRACT_DESCRIPTION contractDescriptionICalculator =
{
    WsCountOf(serviceOperationsICalculator),
    serviceOperationsICalculator
};
```

Tabella delle funzioni

Tabella di funzioni è uno struct di puntatori a funzione che rappresentano ognuna delle operazioni [del servizio](service-operation.md) nel contratto di servizio. La definizione della tabella della funzione viene generata anche [ dawsutil.exe](web-service-compiler-tool.md).

Esempio: Tabella di funzioni

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

Utilizzo del [ **CALLBACK DI RICEZIONE DEL MESSAGGIO \_ DEL \_ \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)

[**WS \_ SERVICE \_ MESSAGE RECEIVE CALLBACK \_ \_ ha**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) un ruolo che si escludono a vicenda.

Se in [**WS \_ SERVICE \_ CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)viene specificata una [**WS \_ CONTRACT \_ DESCRIPTION,**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) questo diventa il gestore di messaggi predefinito per tutte le azioni non supportate dall'elemento **WS CONTRACT DESCRIPTION \_ \_ specificato.** In caso contrario, se **WS \_ CONTRACT \_ DESCRIPTION** non è specificato [](ws-message.md) in WS SERVICE **\_ \_ CONTRACT** e WS SERVICE MESSAGE RECEIVE [**\_ \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback) viene specificato in **WS SERVICE \_ \_ CONTRACT** tutti i messaggi in arrivo vengono passati a questo callback.

Per altri esempi, vedere

-   [Esempio di servizio non tipiato](untypedserviceexample.md)
-   [Esempio di servizio Calculator](httpcalculatorserviceexample.md)
-   [Operazioni del servizio](service-operation.md)

I callback seguenti fanno parte del contratto:

-   [**CALLBACK DI \_ RICEZIONE DEI MESSAGGI DEL \_ \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**CALLBACK \_ \_ STUB DEL SERVIZIO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)

Le strutture seguenti fanno parte del contratto:

-   [**DESCRIZIONE DEL CONTRATTO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description)
-   [**CONTRATTO DI SERVIZIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract)

 

 




