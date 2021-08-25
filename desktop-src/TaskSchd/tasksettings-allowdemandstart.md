---
title: TaskSettings.AllowDemandStart - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Proprietà AllowDemandStart Utilità di pianificazione
- Proprietà AllowDemandStart Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà , AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48ecaf9010b4269ffff66b556d01cfccc057fd05207f619290af9e50f6c757f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959481"
---
# <a name="tasksettingsallowdemandstart-property"></a>TaskSettings.AllowDemandStart - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se True, l'attività può essere eseguita usando il comando Esegui o il menu di scelta rapida. Se False, l'attività non può essere eseguita usando il comando Esegui o il menu di scelta rapida. Il valore predefinito è True.

## <a name="remarks"></a>Commenti

Quando questa proprietà è impostata su True, l'attività può essere avviata indipendentemente dall'avvio dell'attività da parte di qualsiasi trigger.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata [nell'elemento AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) dello schema Utilità di pianificazione attività.

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

 

 





