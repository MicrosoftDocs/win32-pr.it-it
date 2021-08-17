---
title: Metodo RegisteredTask.GetRunTimes
description: Per lo scripting, ottiene gli orari in cui è pianificata l'esecuzione dell'attività registrata durante un periodo di tempo specificato.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Metodo GetRunTimes Utilità di pianificazione
- Metodo GetRunTimes Utilità di pianificazione , oggetto RegisteredTask
- Metodo RegisteredTask Utilità di pianificazione , GetRunTimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303dd08c576f31946207241b086fe945b3f1ac275c596496139d19f507670e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759666"
---
# <a name="registeredtaskgetruntimes-method"></a>Metodo RegisteredTask.GetRunTimes

Per lo scripting, ottiene gli orari in cui è pianificata l'esecuzione dell'attività registrata durante un periodo di tempo specificato.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*begin* \[ Pollici\]
</dt> <dd>

Ora di inizio della query.

</dd> <dt>

*end* \[ Pollici\]
</dt> <dd>

Ora di fine della query.

</dd> <dt>

*count* \[ Cambio\]
</dt> <dd>

Numero di volte pianificate per l'esecuzione dell'attività.

</dd> <dt>

*rgstTaskTimes* \[ Cambio\]
</dt> <dd>

Orari pianificati per l'esecuzione dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

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

 

 





