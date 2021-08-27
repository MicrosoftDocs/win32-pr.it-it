---
title: Elemento SessionStateChangeTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando viene modificato lo stato di una sessione di Terminal Server.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Elemento SessionStateChangeTrigger Utilità di pianificazione
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099821"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Elemento SessionStateChangeTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando viene modificato lo stato di una sessione di Terminal Server.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

**L'elemento SessionStateChangeTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                      | Tipo                                                                                    | Descrizione                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Specifica un valore che indica la lunghezza del ritardo prima dell'avvio di un'attività quando viene rilevata una modifica dello stato della sessione di Terminal Server.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Specifica il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Specifica l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.<br/>              |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, viene specificato un trigger di modifica dello stato della sessione usando [**l'oggetto SessionStateChangeTrigger.**](sessionstatechangetrigger.md)

Per lo sviluppo in C++, un trigger di modifica dello stato della sessione viene specificato usando [**l'interfaccia ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





