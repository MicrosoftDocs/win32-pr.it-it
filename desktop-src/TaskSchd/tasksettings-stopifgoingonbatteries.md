---
title: TaskSettings.StopIfGoingOnBatteries - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer sta caricando batterie.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Proprietà StopIfGoingOnBatteries Utilità di pianificazione
- Proprietà StopIfGoingOnBatteries Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229d5d3beef974e9ce8758f9bd81fc3217bd9c3fcf9bf37be137abe6515cc62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974887"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>TaskSettings.StopIfGoingOnBatteries - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer sta caricando batterie.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica che l'attività verrà arrestata se il computer sta caricando batterie. Se True, la proprietà indica che l'attività verrà arrestata se il computer sta caricando batterie. Se False, la proprietà indica che l'attività non verrà arrestata se il computer sta caricando batterie. Il valore predefinito è True. Per altri dettagli, vedere Note.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata [**nell'elemento StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) dello schema Utilità di pianificazione dati.

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

 

 





