---
title: Metodo INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator.h)
description: Consente ai validator di integrità del sistema (SHV) di impostare SoHResponse da inviare alla controparte dell'agente di integrità del sistema (SHA) sul lato client.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Metodo SetSoHResponse NAP
- Metodo SetSoHResponse NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af44bc3c4801a35ad311f184f3aa2763ccc401ee01dce8a96ef65a0e2496219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939139"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>Metodo INapSystemHealthValidationRequest::SetSoHResponse

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest::SetSoHResponse** consente ai validator di integrità del sistema (SHV) di impostare [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) da inviare alla controparte dell'agente di integrità del sistema (SHA) sul lato client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SoHResponse.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





