---
title: Elemento TimeTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando il trigger viene attivato.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Elemento TimeTrigger Utilità di pianificazione
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6b766a64f87b43feb23200176c5d23e254638a0022ea4d77b64264ca1d507d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355848"
---
# <a name="timetrigger-triggergroup-element"></a>Elemento TimeTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando il trigger viene attivato.

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

**L'elemento TimeTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                        | Tipo                                                                     | Descrizione                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Enabled (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Specifica l'intervallo di tempo massimo durante il quale l'attività può essere avviata dal trigger.<br/>                                   |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**tipo di ripetizione**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Specifica la data e l'ora di attivazione del trigger. Questo elemento è obbligatorio.<br/>                                    |



## <a name="attributes"></a>Attributi



| Nome | Tipo       | Descrizione                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

[**L'elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger di ora e calendario (**TimeTrigger** [**e CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Per lo sviluppo di script, viene specificato un trigger temporale usando [**l'oggetto TimeTrigger.**](timetrigger.md)

Per lo sviluppo in C++, viene specificato un trigger temporale usando [**l'interfaccia ITimeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)

Gli elementi figlio elencati in precedenza sono definiti dai tipi di [**elemento complessi triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md) Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Enabled (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger temporale, vedere [Esempio di trigger temporale (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





