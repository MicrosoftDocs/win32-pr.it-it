---
title: TaskSettings.RestartInterval - proprietà
description: Per lo scripting, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Proprietà RestartInterval Utilità di pianificazione
- Proprietà RestartInterval Utilità di pianificazione, oggetto TaskSettings
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
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734146"
---
# <a name="tasksettingsrestartinterval-property"></a>TaskSettings.RestartInterval - proprietà

Per lo scripting, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valore proprietà

Valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività. Se questa proprietà è impostata, deve essere impostata anche la proprietà [**RestartCount.**](tasksettings-restartcount.md) Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata [**nell'elemento Interval**](taskschedulerschema-interval-restarttype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





