---
title: Interfaccia INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Vengono utilizzati per supportare i validator di integrità del sistema definiti dallo sviluppatore di applicazioni.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- NAP interfaccia INapSystemHealthValidationRequest
- Interfaccia NAP di INapSystemHealthValidationRequest, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743535"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>Interfaccia INapSystemHealthValidationRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapSystemHealthValidationRequest** fornisce i metodi utilizzati per supportare i validator dell'integrità di sistema definiti dallo sviluppatore di applicazioni.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthValidationRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidationRequest** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthValidationRequest** dispone di questi metodi.



| Metodo                                                                                                                               | Descrizione                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest::GetCorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Utilizzato dai validator per recuperare l'ID di correlazione. Il validator deve quindi registrare queste informazioni.<br/>           |
| [**INapSystemHealthValidationRequest:: GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Utilizzato dai validator per recuperare il nome del computer. Il validator deve quindi registrare queste informazioni.<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Consente al NapServer di recuperare le informazioni sullo stato.<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Consente ai validator di recuperare e convalidare le informazioni SoHRequest.<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Ottiene l'oggetto SoHResponse.<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Utilizzato dai validator per recuperare un identificatore univoco di Exchange. Il validator deve quindi registrare queste informazioni.<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Consente all'NapServer di archiviare le informazioni sullo stato.<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Consente ai validator di impostare SoHResponse.<br/>                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

