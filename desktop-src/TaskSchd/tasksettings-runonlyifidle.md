---
title: Proprietà TaskSettings. RunOnlyIfIdle
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Utilità di pianificazione proprietà RunOnlyIfIdle
- Utilità di pianificazione proprietà RunOnlyIfIdle, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RunOnlyIfIdle
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
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400466"
---
# <a name="tasksettingsrunonlyifidle-property"></a>Proprietà TaskSettings. RunOnlyIfIdle

Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, la proprietà indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





