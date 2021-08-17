---
title: RunningTask.EnginePID - proprietà
description: Per lo scripting, ottiene l'ID processo per il motore (processo) che esegue l'attività.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Proprietà EnginePID Utilità di pianificazione
- Proprietà EnginePID Utilità di pianificazione , oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione , proprietà EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed259ccc92e954ae1acde076f0cc09167d15071ea71a33039e7298479875b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759074"
---
# <a name="runningtaskenginepid-property"></a>RunningTask.EnginePID - proprietà

Per lo scripting, ottiene l'ID processo per il motore (processo) che esegue l'attività.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valore proprietà

ID del processo per il motore che esegue l'attività.

## <a name="remarks"></a>Commenti

L'ID processo restituito da questa proprietà non può essere aggiunto direttamente a una stringa. Il valore restituito deve prima essere convertito in un valore integer chiamando la [funzione CInt](/previous-versions//fctcwhw9(v=vs.85)) sul valore restituito.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

