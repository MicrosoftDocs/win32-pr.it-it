---
title: Proprietà TaskSettings. IdleSettings
description: Per gli script, ottiene o imposta le informazioni che specificano il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Utilità di pianificazione proprietà IdleSettings
- Utilità di pianificazione proprietà IdleSettings, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301995"
---
# <a name="tasksettingsidlesettings-property"></a>Proprietà TaskSettings. IdleSettings

Per gli script, ottiene o imposta le informazioni che specificano il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività. Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IdleSettings**](idlesettings.md) che specifica il modo in cui il utilità di pianificazione gestisce l'attività quando il computer entra in una condizione di inattività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





