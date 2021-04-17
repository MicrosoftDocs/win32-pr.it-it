---
title: Proprietà TaskSettings. RestartCount
description: Per gli script, ottiene o imposta il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Utilità di pianificazione proprietà RestartCount
- Utilità di pianificazione proprietà RestartCount, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400467"
---
# <a name="tasksettingsrestartcount-property"></a>Proprietà TaskSettings. RestartCount

Per gli script, ottiene o imposta il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Valore proprietà

Il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**count**](taskschedulerschema-count-restarttype-element.md) dello schema utilità di pianificazione.

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

 

 





