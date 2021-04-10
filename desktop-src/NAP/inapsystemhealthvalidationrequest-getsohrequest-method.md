---
title: Metodo INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Consente ai validator di integrità del sistema (SHV) di recuperare e convalidare le informazioni SoHRequest inviate dalle relative controparti Agente integrità sistema nel client.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- NAP metodo GetSoHRequest
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
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121595"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>Metodo INapSystemHealthValidationRequest:: GetSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest:: GetSoHRequest** consente ai validator di integrità del sistema (SHV) di recuperare e convalidare le informazioni [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) inviate dalle controparti dell'agente integrità sistema (SHA) sul client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*napSystemGenerated* \[ out\]
</dt> <dd>

**Bool** che è **true** se il rapporto di integrità è stato creato da NAPAGENT per conto dell'SHA e **false** in caso contrario. Viene utilizzato principalmente per indicare un errore SHA per il servizio di convalida dell'integrità di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il parametro *sohRequest* può restituire **null** se il client non ha inviato un [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al servizio di convalida dell'integrità di sistema. In questo scenario, il servizio di convalida dell'integrità di sistema può popolare un **SoHResponse** con il codice di errore [**NAP \_ E \_ Missing \_ SOH**](nap-error-constants.md).

Se il parametro *napSystemGenerated* è **true**, il formato di *SoHRequest* è il seguente:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<Sha-Failure-Error-Code>**](nap-error-constants.md)

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

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





