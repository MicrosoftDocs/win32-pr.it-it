---
title: Operazione del servizio
description: L'operazione del servizio è il codice e i metadati associati a una specifica operazione di un servizio.
ms.assetid: 788940a0-b1d9-45d7-a4b5-6f0926026c7d
keywords:
- Servizi Web per le operazioni di servizio per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e7883c0988189db3d977a78615c024dc92df36
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "103968838"
---
# <a name="service-operation"></a>Operazione del servizio

L'operazione del servizio è il codice e i metadati associati a una specifica operazione di un servizio.


In termini di WSDL, ogni operazione WSDL: definita nel documento WSDL per un oggetto portType specificato è un'operazione del servizio.

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

Ogni operazione del servizio all'interno del modello di servizio viene fornita come [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description). \_ \_ La descrizione dell'operazione WS viene generata dal [wsutil.exe](web-service-compiler-tool.md).

Per ogni elemento WSDL: Operation lo strumento genera una [**\_ \_ Descrizione dell'operazione WS**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)separata.

![Diagramma che illustra come wsutil.exe genera una WS_CONTRACT_DESCRIPTION.](images/porttypetocontract.png)

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

In termini di codice a ogni operazione del servizio è associata una funzione. La definizione di questa funzione è diversa per client e server.

Le operazioni del servizio sono classificate in

-   [Operazioni del servizio lato client](client-side-service-operations.md)
-   [Operazioni del servizio sul lato server](server-side-service-operations.md)

Questa classificazione è basata principalmente sul layout della firma del server e sulle implementazioni lato client delle operazioni del servizio.

Vedere anche la [sezione supporto WSDL](wsdl-support.md).

Con le operazioni del servizio vengono usate le enumerazioni seguenti:

-   [**\_tipo di parametro WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_parameter_type)
-   [**\_ \_ motivo annullamento servizio \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_cancel_reason)
-   [**\_ \_ \_ opzione messaggio operazione servizio \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_charset)

Con le operazioni del servizio vengono utilizzate le strutture seguenti:

-   [**\_Descrizione del messaggio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)
-   [**\_Descrizione dell'operazione WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_operation_description)
-   [**\_Descrizione parametro \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_parameter_description)

 

 




