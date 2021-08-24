---
title: TaskSettings.RestartInterval - proprietà
description: Per lo scripting, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Proprietà RestartInterval Utilità di pianificazione
- Proprietà RestartInterval Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà , RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293072fcec50b140a298887b12ed8f5dd1fb6a298c3b486069fe2e7eccaef00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681611"
---
# <a name="tasksettingsrestartinterval-property"></a>TaskSettings.RestartInterval - proprietà

Per lo scripting, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valore proprietà

Valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività. Se questa proprietà è impostata, è necessario impostare anche la proprietà [**RestartCount.**](tasksettings-restartcount.md) Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) dello schema Utilità di pianificazione schema.

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

 

 





