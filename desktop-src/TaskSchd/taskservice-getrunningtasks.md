---
title: Metodo TaskService.GetRunningTasks
description: Per lo scripting, ottiene una raccolta di attività in esecuzione.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Metodo GetRunningTasks Utilità di pianificazione
- Metodo GetRunningTasks Utilità di pianificazione , oggetto TaskService
- Oggetto TaskService Utilità di pianificazione metodo , GetRunningTasks
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
ms.openlocfilehash: 9ecbc52451a4ed3dcc5f3ecc9984009e94dd9bf18b4c8dc667c0b040c43cc68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072421"
---
# <a name="taskservicegetrunningtasks-method"></a>Metodo TaskService.GetRunningTasks

Per lo scripting, ottiene una raccolta di attività in esecuzione.

> [!Note]  
> **TaskService.GetRunningTasks** restituirà solo una raccolta di attività in esecuzione in o al di sotto del contesto di sicurezza di un utente. Ad esempio, per i membri del gruppo Administrators, **GetRunningTasks** restituirà una raccolta di tutte le attività in esecuzione, ma per i membri del gruppo Users, **GetRunningTasks** restituirà solo una raccolta di attività in esecuzione nel contesto di sicurezza del gruppo Users.

 

## <a name="syntax"></a>Sintassi


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Passare 1 per restituire tutte le attività in esecuzione, incluse le attività nascoste. Passare 0 per restituire una raccolta di attività in esecuzione che non sono attività nascoste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**RunningTaskCollection**](runningtaskcollection.md) che contiene le attività attualmente in esecuzione.

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

 

 





