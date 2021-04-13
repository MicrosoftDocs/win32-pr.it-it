---
title: Metodo INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Consente la convalida dell'integrità di sistema (SHV) per impostare il SoHResponse da inviare alla rispettiva controparte Agente integrità sistema (SHA) sul lato client.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- NAP metodo SetSoHResponse
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
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400822"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>Metodo INapSystemHealthValidationRequest:: SetSoHResponse

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest:: SetSoHResponse** consente ai validator di integrità del sistema (SHV) di impostare il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) da inviare alla rispettiva controparte dell'agente integrità sistema (SHA) sul lato client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ in\]
</dt> <dd>

Puntatore a una struttura [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

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

 

 





