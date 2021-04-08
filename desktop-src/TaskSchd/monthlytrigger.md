---
title: Oggetto MonthlyTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Utilità di pianificazione trigger mensile, oggetto
- Utilità di pianificazione oggetto MonthlyTrigger
- Oggetto MonthlyTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741882"
---
# <a name="monthlytrigger-object"></a>Oggetto MonthlyTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile. Ad esempio, l'attività viene avviata in giorni specifici di mesi specifici.

## <a name="members"></a>Membri

L'oggetto **MonthlyTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **MonthlyTrigger** dispone di queste proprietà.



| Proprietà                                                                     | Tipo di accesso           | Descrizione                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta i giorni del mese durante i quali viene eseguita l'attività.<br/>                                                                                                                   |
| [**Abilitato**](trigger-enabled.md)<br/>                                | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                            | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>          | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.<br/>                           |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                               |
| [**MonthsOfYear**](monthlytrigger-monthsofyear.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.<br/>                                                                                                                  |
| [**RandomDelay**](monthlytrigger-randomdelay.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.<br/>                                                                                               |
| [**Ripetizione**](trigger-repetition.md)<br/>                          | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**RunOnLastDayOfMonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività viene eseguita l'ultimo giorno del mese.<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                              |



 

## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger mensile utilizzando l'elemento [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[Oggetti Utilità di pianificazione](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





