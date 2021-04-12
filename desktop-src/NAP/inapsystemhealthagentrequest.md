---
title: Interfaccia INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: SHAs utilizzare per comunicare e coordinare l'elaborazione con il sistema NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- NAP interfaccia INapSystemHealthAgentRequest
- Interfaccia NAP di INapSystemHealthAgentRequest, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517704"
---
# <a name="inapsystemhealthagentrequest-interface"></a>Interfaccia INapSystemHealthAgentRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapSystemHealthAgentRequest** fornisce i metodi usati da Shas per comunicare e coordinare l'elaborazione con il sistema NAP.

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthAgentRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentRequest** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthAgentRequest** dispone di questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentRequest::GetCacheSoHFlag**](inapsystemhealthagentrequest-getcachesohflag-method.md)               | Utilizzato solo da NapAgent.<br/>                                                            |
| [**INapSystemHealthAgentRequest::GetCorrelationId**](inapsystemhealthagentrequest-getcorrelationid-method.md)             | Utilizzato dagli agenti di integrità del sistema per la correlazione di invieranno e [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).<br/> |
| [**INapSystemHealthAgentRequest::GetSoHRequest**](inapsystemhealthagentrequest-getsohrequest-method.md)                   | Usato da SHAs per ottenere invieranno precedentemente memorizzati nella cache da NapAgent.<br/>                           |
| [**INapSystemHealthAgentRequest::GetSoHResponse**](inapsystemhealthagentrequest-getsohresponse-method.md)                 | Utilizzato dall'agente per l'integrità per recuperare il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).<br/>         |
| [**INapSystemHealthAgentRequest::GetStringCorrelationId**](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | Utilizzato dagli agenti di integrità del sistema per registrare l'ID di correlazione.<br/>                               |
| [**INapSystemHealthAgentRequest::SetSoHRequest**](inapsystemhealthagentrequest-setsohrequest-method.md)                   | Utilizzato dagli agenti di integrità per scrivere la richiesta di rapporto di integrità.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

