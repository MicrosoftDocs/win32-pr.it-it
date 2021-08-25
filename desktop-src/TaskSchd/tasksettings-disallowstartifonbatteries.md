---
title: TaskSettings.DisallowStartIfOnBatteries - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione su batterie.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Proprietà DisallowStartIfOnBatteries Utilità di pianificazione
- Proprietà DisallowStartIfOnBatteries Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà , DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e3e57a961f08a5f1ddae17c8334c9f1d3501b34590b1f98676195108444d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099721"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>TaskSettings.DisallowStartIfOnBatteries - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione su batterie.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione su batterie. Se True, l'attività non verrà avviata se il computer è in esecuzione con batterie. Se False, l'attività verrà avviata se il computer è in esecuzione con batterie. Il valore predefinito è True.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) dello schema Utilità di pianificazione attività.

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

 

 





