---
title: Oggetto MonthlyDOWTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile del giorno della settimana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Utilità di pianificazione trigger DOW mensile, oggetto
- Utilità di pianificazione oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048154"
---
# <a name="monthlydowtrigger-object"></a>Oggetto MonthlyDOWTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile del giorno della settimana. Ad esempio, l'attività viene avviata a ogni primo giovedì, da maggio a ottobre.

## <a name="members"></a>Membri

L'oggetto **MonthlyDOWTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **MonthlyDOWTrigger** dispone di queste proprietà.



| Proprietà                                                                          | Tipo di accesso           | Descrizione                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](monthlydowtrigger-daysofweek.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.<br/>                                                                                                                    |
| [**Abilitato**](trigger-enabled.md)<br/>                                     | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>               | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo durante il quale l'attività avviata da questo trigger può essere eseguita.<br/>                          |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                               |
| [**MonthsOfYear**](monthlydowtrigger-monthsofyear.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.<br/>                                                                                                                  |
| [**RandomDelay**](monthlydowtrigger-randomdelay.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.<br/>                                                                                               |
| [**Ripetizione**](trigger-repetition.md)<br/>                               | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**RunOnLastWeekOfMonth**](monthlydowtrigger-runonlastweekofmonth.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che l'attività viene eseguita l'ultima settimana del mese.<br/>                                                                                    |
| [**StartBoundary**](trigger-startboundary.md)<br/>                         | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                              |
| [**WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.<br/>                                                                                                                  |



 

## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .

Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger di giorno della settimana mensile utilizzando l'elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) dello schema utilità di pianificazione.

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

 

 





