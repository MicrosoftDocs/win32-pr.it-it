---
title: Metodo INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator. h)
description: Recupera SoHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- NAP metodo GetSoHResponse
- Metodo GetSoHResponse NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302502"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a>Metodo INapSystemHealthValidationRequest:: GetSoHResponse

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest:: GetSoHResponse** Recupera il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Puntatore a un puntatore al [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)ricevuto.

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

 

 





