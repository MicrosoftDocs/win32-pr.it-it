---
title: Metodo INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent.h)
description: Viene chiamato da NapAgent per eseguire una query sulla richiesta SoH dell'agente integrità sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Metodo GetSoHRequest NAP
- Metodo GetSoHRequest NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c9203a782be34be66e84fa8238a678647a4359df8cde3408aa8de99e73fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133770"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>Metodo INapSystemHealthAgentCallback::GetSoHRequest

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentCallback::GetSoHRequest** viene chiamato da NapAgent per eseguire una query sulla richiesta SoH dell'agente integrità del sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
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



| Codice restituito                                                                                                                      | Descrizione                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                             | Indica l'esito positivo dell'operazione.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ DA \_ WIN32 (SERVER \_ RPC S NON \_ \_ DISPONIBILE)**</dt> </dl> | Se questo codice viene restituito dall'implementazione, NapAgent rimuove l'sha dall'elenco bound-SHA e scarica la voce della cache.<br/> |



 

Quando un valore restituito (ad eccezione di **HRESULT \_ FROM \_ WIN32(RPC \_ S SERVER \_ \_ UNAVAILABLE)**) viene restituito dall'implementazione, il sistema nap costruisce e restituisce [**un SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) alla shv corrispondente con i tipi di attributo e i valori seguenti:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <codice di errore>

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema nap e deve essere implementato dal writer SHA.

Questo metodo deve elaborare la richiesta e restituire immediatamente un valore. Il ritardo della restituzione di questo metodo influisce negativamente sulle prestazioni e sulla velocità di risposta del sistema e può causare il timeout di altre parti del sistema operativo.

Il monitoraggio dello stato di integrità non deve essere eseguito come parte di questa chiamata, soprattutto se è a elevato utilizzo di calcolo e richiede molto tempo. Il monitoraggio dello stato di integrità e il calcolo SoH devono essere eseguiti in un thread o in un servizio separato. L'unica funzione di questo metodo deve essere impostare il soH dell'SHA e restituire.

Se la generazione di un soH da parte dell'SHA può richiedere molto tempo, il file SoH memorizzato nella cache deve essere restituito a NapAgent. Se non è presente alcun SoH memorizzato nella cache da restituire, l'SHA deve restituire immediatamente un soh con i tipi di attributo e i valori seguenti:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NO \_ \_ CACHED \_ SOH**](nap-error-constants.md)

Dopo la generazione del soh, l'SHA deve chiamare [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) per notificare a NapAgent la modifica dell'integrità del sistema.

NapAgent chiama questo metodo per eseguire una query su SoHRequest dell'agente di integrità del sistema. L'SHA può eseguire una query [**sull'oggetto INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passato per i parametri necessari per calcolare SoHRequest. L'SHA deve impostare l'oggetto SoHRequest calcolato nell'oggetto richiesta. L'SHA non deve contenere riferimenti all'oggetto richiesta al termine della chiamata.

Quando questo metodo viene chiamato, se è presente un soh nella cache di NapAgent, viene impostato sull'oggetto richiesta. L'SHA può eseguire una query usando **GetSoHRequest.** Se SHA non imposta un nuovo soh, viene usato quello memorizzato nella cache.

Per le sha non associate registrate con il sistema, il sistema nap costruisce e invia un SoHRequest al shv corrispondente con i tipi di attributo e i valori seguenti:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **PROTEZIONE \_ ACCESSO ALLA RETE E \_ NON \_ INIZIALIZZATA**](nap-error-constants.md)

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

 

 





