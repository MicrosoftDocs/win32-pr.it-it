---
title: Impostazioni (taskType)
description: Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Impostazioni elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea754aa883f9c80c4a436357cc159c588bde375aaa66a229b358723b74b9e070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002239"
---
# <a name="settings-tasktype-element"></a>Impostazioni (taskType)

Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

**L Impostazioni** elemento è definito dal [**tipo complesso taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Specifica l'attività eseguita dal servizio Utilità di pianificazione servizio.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                          | Tipo                                                                                              | Descrizione                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Specifica che l'attività può essere terminata usando TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Specifica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Specifica la quantità di tempo di attesa dell'Utilità di pianificazione prima dell'eliminazione dell'attività dopo la scadenza.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Specifica che l'attività non verrà avviata se il computer è in esecuzione con batterie.<br/>                      |
| [**Abilitato**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Specifica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è True.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Periodo di tempo consentito per completare l'attività.<br/>                                                              |
| [**Nascosto**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in stato di inattività.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Specifica il modo in cui Utilità di pianificazione le attività durante la manutenzione automatica.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Specifica il livello di priorità per l'attività.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività ha esito negativo per qualsiasi motivo.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Specifica che l'attività viene eseguita solo quando il computer è in stato di inattività.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Specifica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Specifica che l'Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorsa l'ora pianificata.<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Specifica che l'attività verrà arrestata se il computer sta caricando batterie.<br/>                          |
| [**Volatile**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | Specifica se l'attività viene disabilitata automaticamente Utilità di pianificazione all'Windows avvio.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Specifica che Utilità di pianificazione riattivazione del computer quando è il momento di eseguire l'attività.<br/>                     |



## <a name="remarks"></a>Commenti

È possibile selezionare uno o più elementi figlio a cui si fa riferimento in precedenza.

Per lo sviluppo C++, le informazioni di registrazione di un'attività vengono specificate [**usando Impostazioni proprietà di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Per lo sviluppo di script, le informazioni di registrazione di un'attività vengono specificate usando la [**proprietà TaskDefinition.Impostazioni.**](taskdefinition-settings.md)

## <a name="examples"></a>Esempio

Nell'esempio di codice XML seguente viene definito un elemento settings che consente una terminazione rigida dell'attività.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Per altre informazioni e un esempio completo del codice XML per l'impostazione delle impostazioni dell'attività, vedere [Time Trigger Example (XML) ( Esempio di trigger temporale (XML)](time-trigger-example--xml-.md).

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

 

 





