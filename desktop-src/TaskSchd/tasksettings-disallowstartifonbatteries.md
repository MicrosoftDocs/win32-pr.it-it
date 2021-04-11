---
title: Proprietà TaskSettings. DisallowStartIfOnBatteries
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Utilità di pianificazione proprietà DisallowStartIfOnBatteries
- Utilità di pianificazione proprietà DisallowStartIfOnBatteries, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà DisallowStartIfOnBatteries
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
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120882"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>Proprietà TaskSettings. DisallowStartIfOnBatteries

Per gli script, ottiene o imposta un valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie. Se true, l'attività non verrà avviata se il computer è in esecuzione sulle batterie. Se false, l'attività verrà avviata se il computer è in esecuzione sulle batterie. Il valore predefinito è True.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





