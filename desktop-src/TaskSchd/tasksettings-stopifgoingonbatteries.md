---
title: Proprietà TaskSettings. StopIfGoingOnBatteries
description: Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer sta per accedere alle batterie.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Utilità di pianificazione proprietà StopIfGoingOnBatteries
- Utilità di pianificazione proprietà StopIfGoingOnBatteries, oggetto TaskSettings
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
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478353"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>Proprietà TaskSettings. StopIfGoingOnBatteries

Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività verrà arrestata se il computer sta per accedere alle batterie.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica che l'attività verrà arrestata se il computer sta per accedere alle batterie. Se true, la proprietà indica che l'attività verrà arrestata se il computer sta per accedere alle batterie. Se false, la proprietà indica che l'attività non verrà arrestata se il computer sta per accedere alle batterie. Il valore predefinito è True. Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





