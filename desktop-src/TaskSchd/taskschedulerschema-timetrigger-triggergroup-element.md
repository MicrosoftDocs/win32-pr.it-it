---
title: Elemento TimeTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando viene attivato il trigger.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Utilità di pianificazione elemento TimeTrigger
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478161"
---
# <a name="timetrigger-triggergroup-element"></a>Elemento TimeTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando viene attivato il trigger.

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

L'elemento **TimeTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                        | Tipo                                                                     | Descrizione                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.<br/>                                   |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Specifica la data e l'ora di attivazione del trigger. Questo elemento è obbligatorio.<br/>                                    |



## <a name="attributes"></a>Attributi



| Nome | Tipo       | Descrizione                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Time e Calendar (**TimeTrigger** e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Per lo sviluppo di script, viene specificato un trigger time utilizzando l'oggetto [**TimeTrigger**](timetrigger.md) .

Per lo sviluppo in C++, viene specificato un trigger Time usando l'interfaccia [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .

Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) . Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di ora, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





