---
title: Metodo INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: Viene chiamato da NapAgent per eseguire una query sulla richiesta di rapporto di integrità dell'agente integrità sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- NAP metodo GetSoHRequest
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
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400713"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>Metodo INapSystemHealthAgentCallback:: GetSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentCallback:: GetSoHRequest** viene chiamato da napagent per eseguire una query sulla richiesta di integrità dell'agente integrità sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
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



| Codice restituito                                                                                                                      | Descrizione                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                             | Indica l'esito positivo dell'operazione.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ da \_ Win32 ( \_ server RPC \_ non \_ disponibile)**</dt> </dl> | Se questo codice viene restituito dall'implementazione, NapAgent rimuove l'SHA dall'elenco Bound-SHA e Scarica la voce della cache.<br/> |



 

Quando un valore restituito (ad eccezione di **HRESULT \_ da \_ Win32 (server RPC non \_ \_ \_ disponibile)**) viene restituito dall'implementazione, il sistema di protezione accesso alla rete crea e restituisce un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) all'oggetto convalida integrità corrispondente con i tipi e i valori di attributo seguenti:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = errore <-codice>

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.

Questo metodo deve elaborare la richiesta e restituire immediatamente un risultato. Ritardare la restituzione di questo metodo influisce negativamente sulle prestazioni e la velocità di risposta del sistema e può causare il timeout di altre parti del sistema operativo.

Il monitoraggio dello stato di integrità non deve essere eseguito come parte di questa chiamata, soprattutto se si tratta di un utilizzo intensivo del calcolo e richiede molto tempo. Il monitoraggio dello stato di integrità e il calcolo del rapporto di integrità devono essere eseguiti in un thread o un servizio separato. L'unica funzione di questo metodo deve essere quella di impostare il rapporto di integrità SHA e restituire.

Se la generazione di un rapporto di integrità da parte di SHA richiede molto tempo, il rapporto di integrità memorizzato nella cache deve essere restituito a NapAgent. Se non viene restituito alcun rapporto di integrità memorizzato nella cache, l'SHA dovrebbe restituire immediatamente un rapporto di integrità con i tipi e i valori di attributo seguenti:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ nessun rapporto di \_ \_ integrità memorizzato nella cache**](nap-error-constants.md)

Quando è stato generato il rapporto di integrità, SHA deve chiamare [**INapSystemHealthAgentBinding:: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) per notificare al napagent la modifica dell'integrità del sistema.

NapAgent chiama questo metodo per eseguire una query sul SoHRequest dell'agente integrità sistema. SHA può eseguire una query sull'oggetto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passato per i parametri necessari per calcolare il SoHRequest. SHA deve impostare il SoHRequest calcolato nell'oggetto Request. Al termine della chiamata, il SHA non deve conservare riferimenti all'oggetto Request.

Quando questo metodo viene chiamato, se è presente un rapporto di integrità nella cache di NapAgent, viene impostato sull'oggetto Request. SHA può eseguire una query per l'oggetto usando **GetSoHRequest**. Se SHA non imposta un nuovo rapporto di integrità, viene usato il valore memorizzato nella cache.

Per i SHAs non associati registrati con il sistema, il sistema di protezione accesso alla rete crea e invia un SoHRequest al servizio di convalida dell'integrità di sistema corrispondente con i tipi e i valori di attributo seguenti:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ non \_ inizializzato**](nap-error-constants.md)

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

 

 





