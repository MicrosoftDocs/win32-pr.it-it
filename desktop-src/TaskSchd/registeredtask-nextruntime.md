---
title: RegisteredTask.NextRunTime - proprietà
description: Per lo scripting, ottiene l'ora della successiva esecuzione pianificata dell'attività registrata.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Proprietà NextRunTime Utilità di pianificazione
- Proprietà NextRunTime Utilità di pianificazione , oggetto RegisteredTask
- Proprietà RegisteredTask Utilità di pianificazione , NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850c0215555fd24b729b1d71acaff9fa7083c0f53289f28e4228b8e57ff40e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060049"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask.NextRunTime - proprietà

Per lo scripting, ottiene l'ora della successiva esecuzione pianificata dell'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valore proprietà

Ora della successiva esecuzione pianificata dell'attività registrata.

## <a name="remarks"></a>Commenti

Se l'attività registrata contiene trigger disabilitati singolarmente, questi trigger influiranno comunque sulla successiva ora di esecuzione pianificata restituita anche se sono disabilitati.

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





