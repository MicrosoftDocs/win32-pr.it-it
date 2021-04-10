---
title: Metodo INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: Viene chiamato quando NapAgent riceve un SoHResponse destinato a questo agente per l'integrità.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- NAP metodo ProcessSoHResponse
- Metodo ProcessSoHResponse NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964360"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>INapSystemHealthAgentCallback::P metodo rocessSoHResponse

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentCallback::P rocesssohresponse** viene chiamato quando napagent riceve un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a questo agente per l'integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*richiesta* \[ in\]
</dt> <dd>

Puntatore COM a un oggetto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) che identifica l'oggetto Request.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                            | Descrizione                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Indica l'esito positivo dell'operazione.<br/>                                                            |
| <dl> <dt>**NAP \_ E \_ pacchetto non valido \_**</dt> </dl> | Restituito da questa implementazione se la risposta non è nel formato corretto.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.

Quando NapAgent riceve un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a questo agente per l'integrità, richiama questo metodo. L'agente di integrità deve eseguire una query su SoHResponse dall'oggetto Request. Al termine della chiamata, non devono essere presenti riferimenti all'oggetto Request.

Il metodo **INapSystemHealthAgentCallback::P rocesssohresponse** non deve essere bloccato. Se è necessaria un'elaborazione di correzione, qualsiasi implementazione di **ProcessSoHResponse** deve avviare un nuovo thread per eseguire l'elaborazione della correzione. NapAgent deve chiamare [**INapSystemHealthAgentCallBack:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) per determinare lo stato di correzione dell'SHA.

Questo metodo deve restituire **un \_ \_ \_ pacchetto NAP E non valido** se la risposta non è nel formato corretto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





