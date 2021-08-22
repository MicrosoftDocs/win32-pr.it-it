---
title: Oggetto trigger
description: Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- trigger Utilità di pianificazione , oggetto trigger
- Attivare l'Utilità di pianificazione
- Trigger object Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b27427bf77465be119fc678cb4babf85254fa437b350c54d4409c0cd5b28024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002009"
---
# <a name="trigger-object"></a>Oggetto trigger

Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.

## <a name="members"></a>Membri

**L'oggetto Trigger** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Trigger** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attivato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la quantità massima di tempo consentita per l'esecuzione dell'attività avviata dal trigger.<br/>                                         |
| [**Id**](trigger-id.md)<br/>                                 | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta la data e l'ora di attivazione del trigger. Il trigger può avviare l'attività dopo l'attivazione del trigger.<br/>             |
| [**Tipo**](trigger-type.md)<br/>                             |                       | Ottiene il tipo del trigger.<br/>                                                                                                            |



 

## <a name="remarks"></a>Commenti

Il Utilità di pianificazione fornisce i singoli oggetti seguenti per i diversi trigger che possono essere utilizzati da un'attività:

-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)

Durante la lettura o la scrittura di codice XML, i trigger di un'attività vengono specificati [**nell'elemento Triggers**](taskschedulerschema-triggers-tasktype-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Triggercollection**](triggercollection.md)
</dt> </dl>

 

 





