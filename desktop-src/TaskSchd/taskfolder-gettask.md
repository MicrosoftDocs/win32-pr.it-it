---
title: Proprietà TaskFolder. GetTask
description: Per gli script, ottiene un'attività in una posizione specificata in una cartella.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Utilità di pianificazione proprietà GetTask
- Utilità di pianificazione proprietà GetTask, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà GetTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740599"
---
# <a name="taskfoldergettask-property"></a>Proprietà TaskFolder. GetTask

Per gli script, ottiene un'attività in una posizione specificata in una cartella.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valore proprietà

Percorso (percorso) dell'attività in una cartella. La cartella radice dell'attività è specificata con una barra rovesciata ( \) . Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

## <a name="error-codes"></a>Codici di errore

Attività nella posizione specificata. L'attività è un oggetto [**RegisteredTask**](registeredtask.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





