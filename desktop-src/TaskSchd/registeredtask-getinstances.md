---
title: Metodo RegisteredTask. GetInstances
description: Per gli script, restituisce tutte le istanze attualmente in esecuzione dell'attività registrata.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Metodo GetInstances Utilità di pianificazione
- Metodo GetInstances Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, Metodo GetInstances
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
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120814"
---
# <a name="registeredtaskgetinstances-method"></a>Metodo RegisteredTask. GetInstances

Per gli script, restituisce tutte le istanze attualmente in esecuzione dell'attività registrata.

> [!Note]  
> **RegisteredTask. GetInstances** restituirà solo le istanze dell'attività registrata attualmente in esecuzione che sono in esecuzione nel contesto di sicurezza di un utente o al di sotto di esso. Per i membri del gruppo **Administrators, ad** esempio **, vengono** restituite tutte le istanze dell'attività registrata attualmente in esecuzione, ma per i membri del gruppo Users verranno restituite solo le istanze dell'attività registrata attualmente in esecuzione nel contesto di sicurezza del gruppo Users.

 

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

Questo parametro è riservato per utilizzi futuri e deve essere impostato su 0.

</dd> <dt>

*runningTasks* \[ out\]
</dt> <dd>

Oggetto [**RunningTaskCollection**](runningtaskcollection.md) che contiene tutte le istanze attualmente in esecuzione dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

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

 

 





