---
title: Oggetto IdleTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Utilità di pianificazione Trigger inattivo, oggetto
- Utilità di pianificazione oggetto IdleTrigger
- Oggetto IdleTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302495"
---
# <a name="idletrigger-object"></a>Oggetto IdleTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività. Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.

## <a name="members"></a>Membri

L'oggetto **IdleTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **IdleTrigger** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo in cui l'attività può essere avviata dal trigger.<br/>                                                 |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                                            |



 

## <a name="remarks"></a>Commenti

Un trigger inattivo attiverà un'azione dell'attività solo se il computer entra in uno stato di inattività dopo il limite di inizio del trigger.

Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger inattivo mediante l'elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) dello schema utilità di pianificazione.

Se un'attività viene attivata da un trigger inattivo, la proprietà [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) viene ignorata.

Se l'istanza iniziale di un'attività con un trigger inattivo è ancora in esecuzione, l'attività viene avviata una sola volta senza ripetizioni, anche se nella proprietà di [**ripetizione**](trigger-repetition.md) viene definito più ripetizioni. Questo comportamento non si verifica se l'attività si interrompe da sola.

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
</dt> </dl>

 

 





