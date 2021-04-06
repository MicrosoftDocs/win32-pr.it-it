---
title: Proprietà RegisteredTask. NextRunTime
description: Per lo scripting, ottiene l'ora in cui l'attività registrata viene pianificata per l'esecuzione successiva.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Utilità di pianificazione Proprietà NextRunTime
- Utilità di pianificazione Proprietà NextRunTime, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, Proprietà NextRunTime
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
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742778"
---
# <a name="registeredtasknextruntime-property"></a>Proprietà RegisteredTask. NextRunTime

Per lo scripting, ottiene l'ora in cui l'attività registrata viene pianificata per l'esecuzione successiva.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valore proprietà

Ora pianificata per l'esecuzione successiva dell'attività registrata.

## <a name="remarks"></a>Commenti

Se l'attività registrata contiene trigger disabilitati singolarmente, questi trigger avranno comunque effetto sul successivo runtime pianificato che viene restituito anche se sono disabilitati.

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





