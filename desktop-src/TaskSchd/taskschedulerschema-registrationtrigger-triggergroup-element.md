---
title: Elemento RegistrationTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando l'attività viene registrata.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- trigger di registrazione Utilità di pianificazione, elemento XML
- Elemento RegistrationTrigger Utilità di pianificazione
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 548ffec6bf5982aac407905d944d029b222b741c0c03fe66645f68e771c87342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099971"
---
# <a name="registrationtrigger-triggergroup-element"></a>Elemento RegistrationTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando l'attività viene registrata.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

**L'elemento RegistrationTrigger** è definito dal tipo complesso [**registrationTriggerType.**](taskschedulerschema-registrationtriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                        | Tipo                                                                     | Descrizione                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Specifica il periodo di tempo tra la registrazione dell'attività e l'avvio dell'attività.<br/>                          |
| [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo la disattivazione.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Specifica la quantità massima di tempo durante la quale l'attività può essere avviata dal trigger.<br/>                                   |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Specifica la data e l'ora di attivazione del trigger.<br/>                                                              |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                           |
|------|------|---------------------------------------|
| Id   | ID   | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, viene specificato un trigger di registrazione usando [**l'oggetto RegistrationTrigger.**](registrationtrigger.md)

Per lo sviluppo C++, viene specificato un trigger di registrazione tramite [**l'interfaccia IRegistrationTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)

Gli elementi figlio elencati in precedenza sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**registrationTriggerType.**](taskschedulerschema-registrationtriggertype-complextype.md) Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Delay (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di avvio, vedere Esempio di [trigger di registrazione (XML)](registration-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





