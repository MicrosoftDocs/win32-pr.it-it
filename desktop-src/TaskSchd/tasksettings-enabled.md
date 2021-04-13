---
title: Proprietà TaskSettings. Enabled
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Utilità di pianificazione proprietà abilitata
- Utilità di pianificazione proprietà Enabled, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400748"
---
# <a name="tasksettingsenabled-property"></a>Proprietà TaskSettings. Enabled

Per gli script, ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è true.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, l'attività è abilitata. Se false, l'attività non è abilitata.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





