---
title: Metodo INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent.h)
description: Viene usato dall'agente integrità per recuperare il BLOB SoHResponse quando NapAgent chiama INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Metodo GetSoHResponse NAP
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
ms.openlocfilehash: 1d78b67c38f54cfe1e7d342212be897ba1825b619324e6fc4cb5ab9ae4f5c4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621162"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>Metodo INapSystemHealthAgentRequest::GetSoHResponse

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentRequest::GetSoHResponse** viene usato dall'agente integrità per recuperare il BLOB SoHResponse quando NapAgent chiama [**INapSystemHealthAgentCallback::P rocessSoHResponse.**](inapsystemhealthagentcallback-processsohresponse-method.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a un [**pacchetto SoHResponse.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*flag* \[ Cambio\]
</dt> <dd>

Puntatore a un flag che abilita la correzione da parte dell'SHA se il bit [**shaFixup**](nap-type-constants.md) è impostato; in caso contrario, la correzione è disabilitata.



| Valori possibili                                                                                                                                                          | Significato                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | È previsto che l'sha eseere la correzione in base alla risposta. Se questo flag non è impostato, l'SHA non deve eseguire una correzione anche se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indica che non è integro.<br/> |



 

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
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





