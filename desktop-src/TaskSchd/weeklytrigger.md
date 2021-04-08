---
title: Oggetto WeeklyTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- Utilità di pianificazione trigger settimanale, oggetto
- Utilità di pianificazione oggetto WeeklyTrigger
- Oggetto WeeklyTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743850"
---
# <a name="weeklytrigger-object"></a>Oggetto WeeklyTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale. Ad esempio, l'attività inizia alle ore 8:00. in un giorno specifico della settimana o ogni settimana.

## <a name="members"></a>Membri

L'oggetto **WeeklyTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **WeeklyTrigger** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.<br/>                                                                                                                        |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.<br/>                           |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.<br/>                                                                                               |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'intervallo tra le settimane nella pianificazione.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger settimanale usando l'elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere l' [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md).

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

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





