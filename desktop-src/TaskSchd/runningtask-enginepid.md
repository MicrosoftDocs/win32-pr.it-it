---
title: Proprietà RunningTask. EnginePID
description: Per gli script, ottiene l'ID processo per il motore (processo) che esegue l'attività.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Utilità di pianificazione proprietà EnginePID
- Utilità di pianificazione proprietà EnginePID, oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione, proprietà EnginePID
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
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301911"
---
# <a name="runningtaskenginepid-property"></a>Proprietà RunningTask. EnginePID

Per gli script, ottiene l'ID processo per il motore (processo) che esegue l'attività.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valore proprietà

ID del processo per il motore che esegue l'attività.

## <a name="remarks"></a>Commenti

L'ID di processo restituito da questa proprietà non può essere aggiunto direttamente a una stringa. Il valore restituito deve essere convertito in un valore integer prima chiamando la funzione [CInt](/previous-versions//fctcwhw9(v=vs.85)) sul valore restituito.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

