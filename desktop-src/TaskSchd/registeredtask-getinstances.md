---
title: Metodo RegisteredTask.GetInstances
description: Per lo scripting, restituisce tutte le istanze attualmente in esecuzione dell'attività registrata.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Metodo GetInstances Utilità di pianificazione
- Metodo GetInstances Utilità di pianificazione , oggetto RegisteredTask
- Metodo RegisteredTask Utilità di pianificazione , GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f9224922e70242304423950a67bf4acd866d1a551a90f4c9a6dadb94470ba1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126061"
---
# <a name="registeredtaskgetinstances-method"></a>Metodo RegisteredTask.GetInstances

Per lo scripting, restituisce tutte le istanze attualmente in esecuzione dell'attività registrata.

> [!Note]  
> **RegisteredTask.GetInstances** restituirà solo le istanze dell'attività registrata attualmente in esecuzione in o al di sotto del contesto di sicurezza di un utente. Ad esempio, per i membri del gruppo Administrators, **GetInstances** restituirà tutte le istanze dell'attività attualmente in esecuzione registrata, ma per i membri del gruppo Users, **GetInstances** restituirà solo le istanze dell'attività registrata attualmente in esecuzione in esecuzione nel contesto di sicurezza del gruppo Users.

 

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flags* 
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere impostato su 0.

</dd> <dt>

*runningTasks* \[ Cambio\]
</dt> <dd>

Oggetto [**RunningTaskCollection**](runningtaskcollection.md) che contiene tutte le istanze attualmente in esecuzione dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

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

 

 





