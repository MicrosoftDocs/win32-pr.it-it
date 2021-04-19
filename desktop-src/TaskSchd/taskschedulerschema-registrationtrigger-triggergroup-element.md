---
title: Elemento RegistrationTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando l'attività è registrata.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Utilità di pianificazione trigger di registrazione, elemento XML
- Utilità di pianificazione elemento RegistrationTrigger
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302001"
---
# <a name="registrationtrigger-triggergroup-element"></a>Elemento RegistrationTrigger (triggerGroup)

Specifica un trigger che avvia un'attività quando l'attività è registrata.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

L'elemento **RegistrationTrigger** è definito dal tipo complesso [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                        | Tipo                                                                     | Descrizione                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Specifica l'intervallo di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.<br/>                          |
| [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.<br/>                                   |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Specifica la data e l'ora di attivazione del trigger.<br/>                                                              |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                           |
|------|------|---------------------------------------|
| Id   | ID   | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, viene specificato un trigger di registrazione tramite l'oggetto [**RegistrationTrigger**](registrationtrigger.md) .

Per lo sviluppo in C++, viene specificato un trigger di registrazione tramite l'interfaccia [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .

Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) . Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Ritardo (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di avvio, vedere [esempio di trigger di registrazione (XML)](registration-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





