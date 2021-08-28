---
title: Metodo INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator.h)
description: Consente ai validator di integrità del sistema (SHV) di recuperare e convalidare le informazioni SoHRequest inviate dalle controparti di System Health Agent (SHA) nel client.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Metodo GetSoHRequest NAP
- Metodo GetSoHRequest NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c140af202de263e99f0fa8ec72186da6e995ec
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882612"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>Metodo INapSystemHealthValidationRequest::GetSoHRequest

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest::GetSoHRequest** consente ai validator di integrità del sistema (SHV) di recuperare e convalidare le informazioni [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) inviate dalle controparti dell'agente di integrità del sistema (SHA) nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohRequest* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una [**struttura SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*napSystemGenerated* \[ Cambio\]
</dt> <dd>

Valore **BOOL true** **se** il soh è stato creato da NapAgent per conto di SHA e FALSE in caso **contrario.** Viene usato principalmente per indicare un errore SHA per shv.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il *parametro sohRequest* può restituire **NULL** se il client non ha inviato un [**oggetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a SHV. In questo scenario shv può popolare un **SoHResponse** con il codice di errore [**nap E MISSING \_ \_ \_ SOH**](nap-error-constants.md).

Se il *parametro napSystemGenerated* è **TRUE,** il formato di *SoHRequest* è il seguente:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) =  &lt; Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **&lt; sha-failure-error-code &gt;**](nap-error-constants.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





