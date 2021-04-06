---
title: TaskService. GetRunningTasks, metodo
description: Per gli script, ottiene una raccolta di attività in esecuzione.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Utilità di pianificazione del metodo GetRunningTasks
- Metodo GetRunningTasks Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743738"
---
# <a name="taskservicegetrunningtasks-method"></a>TaskService. GetRunningTasks, metodo

Per gli script, ottiene una raccolta di attività in esecuzione.

> [!Note]  
> **TaskService. GetRunningTasks** restituirà solo una raccolta di attività in esecuzione che sono in esecuzione in o al di sotto del contesto di sicurezza di un utente. Per i membri del gruppo Administrators, ad esempio, **GetRunningTasks** restituirà una raccolta di tutte le attività in esecuzione, ma per i membri del gruppo Users, **GetRunningTasks** restituirà solo una raccolta di attività in esecuzione nel contesto di sicurezza del gruppo Users.

 

## <a name="syntax"></a>Sintassi


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ in\]
</dt> <dd>

Passare 1 per restituire tutte le attività in esecuzione, incluse le attività nascoste. Passare 0 per restituire una raccolta di attività in esecuzione che non sono attività nascoste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**RunningTaskCollection**](runningtaskcollection.md) che contiene le attività attualmente in esecuzione.

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

 

 





