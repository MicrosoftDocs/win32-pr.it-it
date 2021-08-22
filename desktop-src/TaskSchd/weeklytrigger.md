---
title: Oggetto WeeklyTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- trigger settimanale Utilità di pianificazione , oggetto
- Oggetto WeeklyTrigger Utilità di pianificazione
- Oggetto WeeklyTrigger Utilità di pianificazione , descritto
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
ms.openlocfilehash: 51eb48b03efb49bd5642909af4b99b99bfb1f7f139b97f8410e0d5f014843ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001799"
---
# <a name="weeklytrigger-object"></a>Oggetto WeeklyTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o ogni altra settimana.

## <a name="members"></a>Membri

**L'oggetto WeeklyTrigger** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto WeeklyTrigger** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.<br/>                                                                                                                        |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo la disattivazione.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la quantità massima di tempo consentita per l'esecuzione dell'attività avviata dal trigger.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta l'identificatore per il trigger.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta un tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger.<br/>                                                                                               |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene il tipo del trigger.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'intervallo tra le settimane nella pianificazione.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata viene impostata dalla [**proprietà StartBoundary.**](trigger-startboundary.md)

Quando si legge o si scrive codice XML personalizzato per un'attività, viene specificato un trigger settimanale usando l'elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e un esempio di codice per questo oggetto di scripting, vedere [Weekly Trigger Example (Scripting) .](weekly-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





