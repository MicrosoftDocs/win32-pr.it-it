---
title: Interfaccia INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: Sono dichiarati dal sistema e implementati dal writer SHA in modo che NapAgent possa comunicare con l'SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- NAP interfaccia INapSystemHealthAgentCallback
- Interfaccia NAP di INapSystemHealthAgentCallback, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302256"
---
# <a name="inapsystemhealthagentcallback-interface"></a>Interfaccia INapSystemHealthAgentCallback

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapSystemHealthAgentCallback** fornisce metodi di callback dichiarati dal sistema e implementati dal writer Sha in modo che napagent possa comunicare con l'SHA.

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthAgentCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthAgentCallback** dispone di questi metodi.



| Metodo                                                                                                                                           | Descrizione                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Usato dall'SHA per confrontare invieranno.<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Chiamato da NapAgent per determinare lo stato dell'SHA.<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Chiamato da NapAgent per eseguire una query sulla richiesta di rapporto di integrità SHA.<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Chiamato se è stata eseguita una query sul rapporto di integrità dall'SHA, ma la risposta non è mai stata restituita.<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Chiamato da NapAgent per indicare che è stato modificato lo stato di isolamento del sistema o l'ora di fine della prova.<br/> |
| [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Chiamato quando NapAgent riceve una risposta a rapporto di integrità destinata a questo agente integrità.<br/>                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

