---
title: Oggetto TimeTrigger (Windows.applicationmodel.background.h)
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in una data e un'ora specifiche.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- trigger temporale Utilità di pianificazione , oggetto
- Oggetto TimeTrigger Utilità di pianificazione
- Oggetto TimeTrigger Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f0fb6f5eaff5101f3cc1f5c4aeb2245335e4f65b27d2fafb364df2d05618ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771981"
---
# <a name="timetrigger-object"></a>Oggetto TimeTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività in una data e un'ora specifiche.

## <a name="members"></a>Membri

**L'oggetto TimeTrigger** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto TimeTrigger** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attivato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato da [**Trigger**](trigger.md). Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato da [**Trigger**](trigger.md). Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato da [**Trigger**](trigger.md). Ottiene o imposta la quantità massima di tempo consentita per l'esecuzione dell'attività avviata dal trigger.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato da [**Trigger**](trigger.md). Ottiene o imposta l'identificatore per il trigger.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lettura/Scrittura<br/> | Ottiene o imposta un ritardo aggiunto in modo casuale all'ora di inizio del trigger.<br/>                                                                                    |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato da [**Trigger**](trigger.md). Ottiene o imposta la frequenza di esecuzione dell'attività e la durata della ripetizione del modello di ripetizione dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato da [**Trigger**](trigger.md). Ottiene o imposta la data e l'ora di attivazione del trigger. Questo elemento è obbligatorio.<br/>                                    |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato da [**Trigger**](trigger.md). Ottiene il tipo del trigger.<br/>                                                                                              |



 

## <a name="remarks"></a>Commenti

[**L'elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger di ora e calendario ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) [**e CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger inattivo usando [**l'elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Windows.applicationmodel.background.h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





