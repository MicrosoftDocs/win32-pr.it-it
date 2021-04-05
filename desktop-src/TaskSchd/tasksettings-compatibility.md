---
title: Proprietà TaskSettings. Compatibility
description: Per lo scripting, ottiene o imposta un valore integer che indica la versione di Utilità di pianificazione un'attività è compatibile con.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Utilità di pianificazione proprietà di compatibilità
- Utilità di pianificazione proprietà di compatibilità, oggetto TaskSettings
- Utilità di pianificazione oggetto TaskSettings, proprietà di compatibilità
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740815"
---
# <a name="tasksettingscompatibility-property"></a>Proprietà TaskSettings. Compatibility

Per lo scripting, ottiene o imposta un valore integer che indica la versione di Utilità di pianificazione un'attività è compatibile con.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>Valore proprietà



| Valore                                                                                                                                                                                                                                         | Significato                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**Attività \_ COMPATIBILITÀ \_ con**</dt> <dt>0</dt> </dl> | L'attività è compatibile con il comando AT.<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**Attività \_ COMPATIBILITÀ \_ V1**</dt> <dt>1</dt> </dl> | L'attività è compatibile con Utilità di pianificazione 1,0.<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**Attività \_ COMPATIBILITÀ \_ v2**</dt> <dt>2</dt> </dl> | L'attività è compatibile con Utilità di pianificazione 2,0.<br/> |



 

## <a name="remarks"></a>Commenti

Per la compatibilità delle attività, impostata tramite la proprietà [**compatibilità**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , è consigliabile impostare solo la \_ compatibilità delle attività \_ V1 se un'attività deve essere accessibile o modificata da un computer Windows XP, Windows Server 2003 o Windows 2000. In caso contrario, è consigliabile usare Utilità di pianificazione compatibilità 2,0 perché l'attività avrà più funzionalità.

Le attività compatibili con il comando AT possono avere un solo trigger di tempo.

Le attività compatibili con Utilità di pianificazione 1,0 possono avere solo un trigger di ora, un trigger LOGON o un trigger di avvio e l'attività può avere solo un'azione eseguibile.

Per ulteriori informazioni sulla compatibilità delle attività, vedere Novità [di utilità di pianificazione](what-s-new-in-task-scheduler.md) e [attività](tasks.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**compatibilità delle attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





