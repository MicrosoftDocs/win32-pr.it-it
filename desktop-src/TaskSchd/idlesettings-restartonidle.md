---
title: Proprietà IdleSettings. RestartOnIdle
description: Per gli script, ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre una condizione di inattività più di una volta.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Utilità di pianificazione proprietà RestartOnIdle
- Utilità di pianificazione proprietà RestartOnIdle, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, proprietà RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301782"
---
# <a name="idlesettingsrestartonidle-property"></a>Proprietà IdleSettings. RestartOnIdle

Per gli script, ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre una condizione di inattività più di una volta.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica se l'attività deve essere riavviata quando il computer scorre in una condizione di inattività più di una volta. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata solo se la proprietà [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) è impostata su true.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) dello schema utilità di pianificazione.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





