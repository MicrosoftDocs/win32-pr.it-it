---
title: Oggetto IdleTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- trigger inattivo Utilità di pianificazione , oggetto
- Oggetto IdleTrigger Utilità di pianificazione
- Oggetto IdleTrigger Utilità di pianificazione , descritto
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
ms.openlocfilehash: 41a3c538dbd04f3eb20a86f495fcf4a8b027b51fbe5cd6443cd8ff3a69ac6ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621141"
---
# <a name="idletrigger-object"></a>Oggetto IdleTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività. Per informazioni sulle condizioni di inattività, vedere [Condizioni di inattività delle attività.](task-idle-conditions.md)

## <a name="members"></a>Membri

**L'oggetto IdleTrigger** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto IdleTrigger** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attivato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta l'intervallo di tempo massimo durante il quale l'attività può essere avviata dal trigger.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene il tipo del trigger.<br/>                                                                                                            |



 

## <a name="remarks"></a>Commenti

Un trigger inattivo attiverà un'azione dell'attività solo se il computer entra in uno stato di inattività dopo il limite di avvio del trigger.

Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger inattivo usando [**l'elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) dello schema Utilità di pianificazione dati.

Se un'attività viene attivata da un trigger inattivo, la [**proprietà IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) viene ignorata.

Se l'istanza iniziale di un'attività con un trigger inattivo è ancora in esecuzione, l'attività viene avviata una sola volta senza ripetizioni, anche se nella proprietà [**Ripetizione**](trigger-repetition.md) sono definite più ripetizioni. Questo comportamento non si verifica se l'attività si arresta da sola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[Utilità di pianificazione oggetti](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





