---
title: Elemento SessionStateChangeTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Utilità di pianificazione elemento SessionStateChangeTrigger
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742754"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Elemento SessionStateChangeTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

L'elemento **SessionStateChangeTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                      | Tipo                                                                                    | Descrizione                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Specifica un valore che indica la lunghezza del ritardo prima che un'attività venga avviata quando viene rilevata una modifica dello stato della sessione Terminal Server.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Specifica il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Specifica l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.<br/>              |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, viene specificato un trigger di modifica dello stato della sessione utilizzando l'oggetto [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .

Per lo sviluppo in C++, un trigger di modifica dello stato della sessione viene specificato tramite l'interfaccia [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





