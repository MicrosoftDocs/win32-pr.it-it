---
title: Metodo INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent.h)
description: Viene chiamato quando NapAgent riceve un oggetto SoHResponse destinato a questo agente di integrità.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Metodo ProcessSoHResponse NAP
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
ms.openlocfilehash: 1f5aaca7833560dbb53422da08ced158bb172610c3bacef931866d74d416fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367756"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>Metodo INapSystemHealthAgentCallback::P rocessSoHResponse

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentCallback::P rocessSoHResponse** viene chiamato quando NapAgent riceve un [**oggetto SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a questo agente di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*richiesta* \[ Pollici\]
</dt> <dd>

Puntatore COM a un [**oggetto INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) che identifica l'oggetto richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                            | Descrizione                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Indica l'esito positivo dell'operazione.<br/>                                                            |
| <dl> <dt>**NAP \_ E PACCHETTO NON \_ \_ VALIDO**</dt> </dl> | Restituito da questa implementazione se la risposta non è nel formato corretto.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema nap e deve essere implementato dal writer SHA.

Quando NapAgent riceve un [**oggetto SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a questo agente integrità, richiama questo metodo. L'agente integrità deve eseguire una query su SoHResponse dall'oggetto richiesta. Non deve contenere riferimenti all'oggetto richiesta al termine della chiamata.

Il **metodo INapSystemHealthAgentCallback::P rocessSoHResponse** non deve bloccarsi. Se è necessaria un'elaborazione di correzione, qualsiasi implementazione di **ProcessSoHResponse** deve avviare un nuovo thread per eseguire l'elaborazione della correzione. NapAgent deve chiamare [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) per determinare lo stato di correzione dell'SHA.

Questo metodo deve restituire **NAP \_ E INVALID \_ \_ PACKET** se la risposta non è nel formato corretto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





