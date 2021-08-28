---
title: TaskSettings.Enabled - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è True.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Impostazione delle proprietà abilitata Utilità di pianificazione
- Proprietà Enabled Utilità di pianificazione, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà Enabled
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
ms.openlocfilehash: 0e7853177aecae963e4899a67d2ba5b39d1eaebdc75e25ce6e14523963a70c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738162"
---
# <a name="tasksettingsenabled-property"></a>TaskSettings.Enabled - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è True.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se True, l'attività è abilitata. Se False, l'attività non è abilitata.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) dello schema Utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





