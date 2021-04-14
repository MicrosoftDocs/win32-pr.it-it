---
title: Metodo RegisteredTask. getruntimes
description: Per gli script, ottiene le ore pianificate per l'esecuzione dell'attività registrata in un determinato periodo di tempo.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Metodo getruntimes Utilità di pianificazione
- Metodo getruntimes Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo getruntimes
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
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518502"
---
# <a name="registeredtaskgetruntimes-method"></a>Metodo RegisteredTask. getruntimes

Per gli script, ottiene le ore pianificate per l'esecuzione dell'attività registrata in un determinato periodo di tempo.

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

*inizia* \[ in\]
</dt> <dd>

Ora di inizio per la query.

</dd> <dt>

*fine* \[ in\]
</dt> <dd>

Ora di fine della query.

</dd> <dt>

*numero* \[ di out\]
</dt> <dd>

Numero di volte pianificate in cui l'attività viene eseguita.

</dd> <dt>

*rgstTaskTimes* \[ out\]
</dt> <dd>

Orari pianificati in cui l'attività viene eseguita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

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

 

 





