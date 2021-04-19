---
title: Oggetto TaskSettings
description: Oggetto di scripting che fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per eseguire l'attività.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Utilità di pianificazione oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, descritto
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
ms.openlocfilehash: 4e7690ba59b4794f952ca3b381fc28247f0dfb4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301140"
---
# <a name="tasksettings-object"></a>Oggetto TaskSettings

Oggetto di scripting che fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per eseguire l'attività.

## <a name="members"></a>Membri

L'oggetto **TaskSettings** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **TaskSettings** dispone di queste proprietà.



| Proprietà                                                                                 | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività può essere avviata tramite il comando Esegui o il menu di scelta rapida.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività può essere terminata utilizzando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).<br/>                                                                                                                                                                                                                                                                               |
| [**Compatibilità**](tasksettings-compatibility.md)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta un valore integer che indica la versione di Utilità di pianificazione un'attività è compatibile con.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo che il Utilità di pianificazione attenderà prima di eliminare l'attività dopo la scadenza.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è alimentato a batteria.<br/>                                                                                                                                                                                                                                                                                        |
| [**Abilitato**](tasksettings-enabled.md)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è true.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo consentita per completare l'attività.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Nascosto**](tasksettings-hidden.md)<br/>                                         | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività non sarà visibile nell'interfaccia utente. Tuttavia, gli amministratori possono eseguire l'override di questa impostazione tramite l'uso di un "Master switch" che rende visibili tutte le attività nell'interfaccia utente.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta le informazioni che specificano il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto impostazioni di rete che contiene un identificatore e un nome del profilo di rete. Se la proprietà [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) di **TaskSettings** è **true** e un propfile di rete viene specificato nella proprietà [**NetworkSettings**](tasksettings-networksettings.md) , l'attività verrà eseguita solo se il profilo di rete specificato è disponibile.<br/> |
| [**Priority**](tasksettings-priority.md)<br/>                                     | Lettura/Scrittura<br/> | Ottiene o imposta il livello di priorità dell'attività.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in uno stato di inattività.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer inizia a funzionare con alimentazione a batteria.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.<br/>                                                                                                                                                                                                                                                                                       |
| [**XmlText**](tasksettings-xmltext.md)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta una definizione in formato XML delle impostazioni dell'attività.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un'attività verrà arrestata 72 ore dopo l'avvio dell'esecuzione. È possibile modificare questa impostazione modificando l'impostazione [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md) .

Durante la lettura o la scrittura di codice XML per un'attività, le impostazioni dell'attività vengono definite nell'elemento [**Settings**](taskschedulerschema-settings-tasktype-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
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

 

