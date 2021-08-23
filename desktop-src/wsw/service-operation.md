---
title: Operazione del servizio
description: L'operazione del servizio è il codice e i metadati associati a un'operazione specifica di un servizio.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Servizi Web dell'operazione del servizio per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acde0c2151dea483a3e82f45c7031fa201614076f7a5ea624926fbe08e7588b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026265"
---
# <a name="service-operation"></a>Operazione del servizio

L'operazione del servizio è il codice e i metadati associati a un'operazione specifica di un servizio.


In termini di WSDL, ogni operazione wsdl:operation definita nel documento WSDL per un determinato portType è un'operazione del servizio.

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

Ogni operazione del servizio all'interno del modello di servizio viene specificata come [**WS \_ OPERATION \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description). WS \_ OPERATION DESCRIPTION viene generato da \_ [wsutil.exe](web-service-compiler-tool.md).

Per ogni wsdl:operation lo strumento genera un'operazione [**WS \_ OPERATION DESCRIPTION \_ separata.**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)

![Diagramma che mostra come wsutil.exe genera un WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

``` syntax
static WS_OPERATION_DESCRIPTION serviceOperationsICalculator[] =
{
    {
        // Add Method
        &messageDescriptionAddICalculator,
        &messageDescriptionAddResponseICalculator,
        WsCountOf(parametersAddICalculator),
        ICalculator_Add_Stub 
    }
};
```

In termini di codice a ogni operazione del servizio è associata una funzione . La definizione di questa funzione è diversa per client e server.

Le operazioni del servizio sono classificate in ,

-   [Operazioni del servizio lato client](client-side-service-operations.md)
-   [Operazioni del servizio lato server](server-side-service-operations.md)

Questa classificazione si basa principalmente sul layout della firma del server e sulle implementazioni lato client delle operazioni del servizio.

Vedere anche la [sezione relativa al supporto WSDL](wsdl-support.md).

Le enumerazioni seguenti vengono usate con le operazioni del servizio:

-   [**TIPO DI PARAMETRO WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**MOTIVO \_ ANNULLAMENTO SERVIZIO WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**OPZIONE DEL MESSAGGIO \_ \_ DELL'OPERAZIONE \_ DEL SERVIZIO \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Le strutture seguenti vengono usate con le operazioni del servizio:

-   [**DESCRIZIONE DEL MESSAGGIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**DESCRIZIONE \_ DELL'OPERAZIONE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**DESCRIZIONE DEL PARAMETRO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




