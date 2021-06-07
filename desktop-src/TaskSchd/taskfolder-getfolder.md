---
title: TaskFolder.GetFolder - proprietà
description: Per lo scripting, ottiene una cartella che contiene le attività in un percorso specificato.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Proprietà GetFolder Utilità di pianificazione
- Proprietà GetFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione proprietà , GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387030"
---
# <a name="taskfoldergetfolder-property"></a>TaskFolder.GetFolder - proprietà

Per lo scripting, ottiene una cartella che contiene le attività in un percorso specificato.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valore proprietà

Percorso (percorso) della cartella. Non usare una barra rovesciata dopo l'ultimo nome di cartella nel percorso. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Il carattere '.' non può essere usato per specificare la cartella attività corrente e '..' Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

## <a name="error-codes"></a>Codici di errore

Cartella nel percorso specificato. La cartella è un [**oggetto TaskFolder.**](taskfolder.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





