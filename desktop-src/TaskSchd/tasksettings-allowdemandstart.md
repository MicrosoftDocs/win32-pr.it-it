---
title: Proprietà TaskSettings. AllowDemandStart
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività può essere avviata tramite il comando Esegui o il menu di scelta rapida.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Utilità di pianificazione proprietà AllowDemandStart
- Utilità di pianificazione proprietà AllowDemandStart, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà AllowDemandStart
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
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400340"
---
# <a name="tasksettingsallowdemandstart-property"></a>Proprietà TaskSettings. AllowDemandStart

Per gli script, ottiene o imposta un valore booleano che indica che l'attività può essere avviata tramite il comando Esegui o il menu di scelta rapida.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, l'attività può essere eseguita tramite il comando Esegui o il menu di scelta rapida. Se false, l'attività non può essere eseguita con il comando Esegui o il menu di scelta rapida. Il valore predefinito è True.

## <a name="remarks"></a>Commenti

Quando questa proprietà è impostata su true, l'attività può essere avviata indipendentemente dall'avvio dell'attività da parte dei trigger.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





