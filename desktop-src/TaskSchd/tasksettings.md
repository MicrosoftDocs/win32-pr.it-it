---
title: Oggetto TaskSettings
description: Oggetto di scripting che fornisce le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Oggetto TaskSettings Utilità di pianificazione
- Oggetto TaskSettings Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- TaskSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a687e82248598d9732e91acfd40e9f3dd4d6d3c3fe6c4954cb8706489c814126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738101"
---
# <a name="tasksettings-object"></a>Oggetto TaskSettings

Oggetto di scripting che fornisce le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.

## <a name="members"></a>Membri

**L'oggetto TaskSettings** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto TaskSettings** ha queste proprietà.



| Proprietà                                                                                 | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività può essere terminata tramite [**TerminateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)<br/>                                                                                                                                                                                                                                                                               |
| [**Compatibilità**](tasksettings-compatibility.md)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta un valore intero che indica la versione di Utilità di pianificazione con cui un'attività è compatibile.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo di attesa Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è alimentato a batteria.<br/>                                                                                                                                                                                                                                                                                        |
| [**Abilitato**](tasksettings-enabled.md)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è True.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo consentita per completare l'attività.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Nascosto**](tasksettings-hidden.md)<br/>                                         | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività non sarà visibile nell'interfaccia utente. Tuttavia, gli amministratori possono eseguire l'override di questa impostazione tramite l'uso di un "cambio master" che rende visibili tutte le attività nell'interfaccia utente.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta le informazioni che specificano come il Utilità di pianificazione esegue attività quando il computer si trova in uno stato di inattività.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto impostazioni di rete che contiene l'identificatore e il nome di un profilo di rete. Se la [**proprietà RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) di **TaskSettings** è **True** e nella proprietà [**NetworkSettings**](tasksettings-networksettings.md) è specificato un propfile di rete, l'attività verrà eseguita solo se il profilo di rete specificato è disponibile.<br/> |
| [**Priority**](tasksettings-priority.md)<br/>                                     | Lettura/Scrittura<br/> | Ottiene o imposta il livello di priorità dell'attività.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta il numero di tentativi di riavvio Utilità di pianificazione'attività da parte dell'utente.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer è in stato di inattività.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorsa l'ora pianificata.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer inizia a funzionare a batteria.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione riattiva il computer quando è il momento di eseguire l'attività.<br/>                                                                                                                                                                                                                                                                                       |
| [**Xmltext**](tasksettings-xmltext.md)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta una definizione in formato XML delle impostazioni dell'attività.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un'attività verrà arrestata 72 ore dopo l'avvio dell'esecuzione. È possibile modificare questa impostazione modificando [**l'impostazione ExecutionTimeLimit.**](tasksettings-executiontimelimit.md)

Durante la lettura o la scrittura di codice XML per un'attività, le impostazioni dell'attività vengono definite [**nell'elemento Impostazioni**](taskschedulerschema-settings-tasktype-element.md) dello schema Utilità di pianificazione.

## <a name="examples"></a>Esempio

Per altre informazioni e un esempio di codice per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

