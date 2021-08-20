---
title: Interfaccia INapSystemHealthValidationRequest (NapSystemHealthValidator.h)
description: Vengono usati per supportare i validator di integrità del sistema definiti dallo sviluppatore dell'applicazione.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- Interfaccia INapSystemHealthValidationRequest nap
- Interfaccia INapSystemHealthValidationRequest nap , descritta
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
ms.openlocfilehash: 2e7b6b2fdc0da8757ddd29b963445c0b984c45d19955c093270cf397fcac14b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133476"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>Interfaccia INapSystemHealthValidationRequest

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapSystemHealthValidationRequest** fornisce metodi usati per supportare i validator dell'integrità del sistema definiti dallo sviluppatore dell'applicazione.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) eredita tutti i metodi di questa interfaccia e deve essere usato.

 

## <a name="members"></a>Membri

**L'interfaccia INapSystemHealthValidationRequest** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidationRequest** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **INapSystemHealthValidationRequest.**



| Metodo                                                                                                                               | Descrizione                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest::GetCorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Utilizzato dai validator per recuperare l'ID correlazione. Il validator deve quindi registrare queste informazioni.<br/>           |
| [**INapSystemHealthValidationRequest::GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Usato dai validator per recuperare il nome del computer. Il validator deve quindi registrare queste informazioni.<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Consente a NapServer di recuperare le informazioni sullo stato.<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Consente ai validator di recuperare e convalidare le informazioni SoHRequest.<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Ottiene l'oggetto SoHResponse.<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Utilizzato dai validator per recuperare un identificatore di scambio univoco. Il validator deve quindi registrare queste informazioni.<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Consente a NapServer di archiviare le informazioni sullo stato.<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Consente ai validator di impostare SoHResponse.<br/>                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

