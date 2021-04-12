---
title: Elemento EventTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Utilità di pianificazione trigger evento, elemento
- Elemento EventTrigger Utilità di pianificazione
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478179"
---
# <a name="eventtrigger-triggergroup-element"></a>Elemento EventTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

L'elemento **EventTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                              | Tipo                                                                     | Descrizione                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Specifica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.<br/>                                |
| [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Specifica la data e l'ora di attivazione del trigger.<br/>                                                              |
| [**Sottoscrizione (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | Specifica la query XPath che identifica l'evento che attiva il trigger.<br/>                                             |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                           |
|------|------|---------------------------------------|
| Id   | ID   | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

È possibile creare un massimo di 500 attività con sottoscrizioni di eventi. Una sottoscrizione di eventi che esegue query per una varietà di eventi può essere usata per attivare un'attività che usa la stessa azione in risposta agli eventi che vengono registrati.

Per lo sviluppo di script, un trigger di evento viene definito dall'oggetto [**EventTrigger**](eventtrigger.md) .

Per lo sviluppo in C++, un trigger di evento viene definito dall'interfaccia [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un trigger di evento, vedere [esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

