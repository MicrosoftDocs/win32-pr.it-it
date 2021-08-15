---
title: Interfaccia INapSystemHealthAgentCallback (NapSystemHealthAgent.h)
description: Vengono dichiarati dal sistema e implementati dal writer SHA in modo che NapAgent possa comunicare con l'SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- Interfaccia INapSystemHealthAgentCallback nap
- Interfaccia INapSystemHealthAgentCallback nap , descritta
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
ms.openlocfilehash: 0d7221dada78494f808ca0b98673b351a3a93c8088cc883bb7ed6324619c8ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799149"
---
# <a name="inapsystemhealthagentcallback-interface"></a>Interfaccia INapSystemHealthAgentCallback

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapSystemHealthAgentCallback** fornisce metodi di callback dichiarati dal sistema e implementati dal writer SHA in modo che NapAgent possa comunicare con l'SHA.

## <a name="members"></a>Membri

**L'interfaccia INapSystemHealthAgentCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **INapSystemHealthAgentCallback.**



| Metodo                                                                                                                                           | Descrizione                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Usato dall'SHA per confrontare i soh.<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Chiamato da NapAgent per determinare lo stato dell'sha.<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Chiamato da NapAgent per eseguire una query sulla richiesta SoH dell'SHA.<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Chiamato se è stata eseguita una query su una richiesta SoH dall'SHA, ma la risposta non è mai tornata.<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Chiamato da NapAgent per indicare che lo stato di isolamento del sistema o l'ora di fine della prova sono stati modificati.<br/> |
| [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Chiamato quando NapAgent riceve una risposta SoH destinata a questo agente di integrità.<br/>                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

