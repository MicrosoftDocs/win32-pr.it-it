---
title: TaskSettings.StartWhenAvailable - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorsa l'ora pianificata.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Proprietà StartWhenAvailable Utilità di pianificazione
- Proprietà StartWhenAvailable Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ed43a04bba63d0e760866684df15c4cae5e80a1b3338d122408756f4cec46e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757924"
---
# <a name="tasksettingsstartwhenavailable-property"></a>TaskSettings.StartWhenAvailable - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorsa l'ora pianificata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se True, la proprietà indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorsa l'ora pianificata. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo alle attività basate sul tempo con un limite finale o alle attività basate sul tempo impostate per la ripetizione infinita.

Le attività avviate dopo il superamento dell'ora pianificata (a causa della proprietà [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) impostata su True) vengono accodati nella coda di attività del servizio Utilità di pianificazione e vengono avviate dopo un ritardo. Il ritardo predefinito è 10 minuti.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) dello schema Utilità di pianificazione dati.

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

 

 





