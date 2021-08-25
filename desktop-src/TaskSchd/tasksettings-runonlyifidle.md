---
title: TaskSettings.RunOnlyIfIdle - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Proprietà RunOnlyIfIdle Utilità di pianificazione
- Proprietà RunOnlyIfIdle Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed423dc4cd34a03bd3b76401284a4d6bfb98270e7c0d0feed0a45046a82e7d3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990821"
---
# <a name="tasksettingsrunonlyifidle-property"></a>TaskSettings.RunOnlyIfIdle - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se True, la proprietà indica che il Utilità di pianificazione eseguirà l'attività solo se il computer è in una condizione di inattività. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





