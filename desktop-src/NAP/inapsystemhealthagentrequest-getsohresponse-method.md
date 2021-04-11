---
title: Metodo INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: Viene usato dall'agente per l'integrità per recuperare il BLOB SoHResponse quando NapAgent chiama INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- NAP metodo GetSoHResponse
- Metodo GetSoHResponse NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119399"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>Metodo INapSystemHealthAgentRequest:: GetSoHResponse

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentRequest:: GetSoHResponse** viene usato dall'agente per l'integrità per recuperare il BLOB SoHResponse quando napagent chiama [**INapSystemHealthAgentCallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Puntatore a un puntatore a un pacchetto [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*flag* \[ out\]
</dt> <dd>

Puntatore a un flag che consente la correzione da parte di SHA se il bit [**shaFixup**](nap-type-constants.md) è impostato; in caso contrario, la correzione è disabilitata.



| Valori possibili                                                                                                                                                          | Significato                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Si prevede che l'SHA esegua la correzione in base alla risposta. Se questo flag non è impostato, SHA non deve eseguire una correzione anche se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indica che non è integro.<br/> |



 

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
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





