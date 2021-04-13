---
title: Settings (taskType)-elemento
description: Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Utilità di pianificazione elemento impostazioni
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400473"
---
# <a name="settings-tasktype-element"></a>Settings (taskType)-elemento

Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

L'elemento **Settings** è definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Specifica l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                          | Tipo                                                                                              | Descrizione                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Specifica che l'attività può essere terminata utilizzando TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Specifica che l'attività può essere avviata utilizzando il comando Esegui o il menu di scelta rapida.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Specifica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.<br/>                      |
| [**Abilitato**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Specifica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è true.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Quantità di tempo consentita per completare l'attività.<br/>                                                              |
| [**Nascosto**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Specifica il modo in cui il Utilità di pianificazione esegue le attività durante la manutenzione automatica.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Specifica il livello di priorità per l'attività.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Specifica che l'attività viene eseguita solo quando il computer è in stato di inattività.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Specifica che l'Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Specifica che l'attività verrà arrestata se il computer sta per accedere alle batterie.<br/>                          |
| [**Volatile**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | Specifica se l'attività viene disabilitata automaticamente da Utilità di pianificazione all'avvio di Windows.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Specifica che Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.<br/>                     |



## <a name="remarks"></a>Commenti

È possibile selezionare uno o più elementi figlio a cui si fa riferimento sopra.

Per lo sviluppo in C++, le informazioni di registrazione di un'attività vengono specificate utilizzando la [**Proprietà Settings di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Per lo sviluppo di script, le informazioni di registrazione di un'attività vengono specificate utilizzando la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) .

## <a name="examples"></a>Esempio

Nell'esempio di codice XML seguente viene definito un elemento Settings che consente la terminazione rigida dell'attività.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Per ulteriori informazioni e un esempio completo del codice XML per l'impostazione delle impostazioni delle attività, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).

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

 

 





