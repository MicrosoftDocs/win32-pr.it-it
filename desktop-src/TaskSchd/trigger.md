---
title: Oggetto trigger
description: Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- trigger Utilità di pianificazione, oggetto trigger
- Utilità di pianificazione oggetto trigger
- Utilità di pianificazione oggetto trigger, descritto
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
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873545"
---
# <a name="trigger-object"></a>Oggetto trigger

Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.

## <a name="members"></a>Membri

L'oggetto **trigger** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **trigger** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.<br/>                                         |
| [**ID**](trigger-id.md)<br/>                                 | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta la data e l'ora di attivazione del trigger. Il trigger può avviare l'attività dopo che il trigger è stato attivato.<br/>             |
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

Durante la lettura o la scrittura di codice XML, i trigger di un'attività vengono specificati nell'elemento [**trigger**](taskschedulerschema-triggers-tasktype-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> </dl>

 

 





