---
title: TaskFolder.GetTask - proprietà
description: Per lo scripting, ottiene un'attività in un percorso specificato in una cartella.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Proprietà GetTask Utilità di pianificazione
- Proprietà GetTask Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione proprietà , GetTask
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387677"
---
# <a name="taskfoldergettask-property"></a>TaskFolder.GetTask - proprietà

Per lo scripting, ottiene un'attività in un percorso specificato in una cartella.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valore proprietà

Percorso (percorso) dell'attività in una cartella. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Il carattere '.' non può essere usato per specificare la cartella attività corrente e '..' Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

## <a name="error-codes"></a>Codici di errore

Attività nella posizione specificata. L'attività è un [**oggetto RegisteredTask.**](registeredtask.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





