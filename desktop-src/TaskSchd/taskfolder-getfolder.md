---
title: Proprietà TaskFolder. GetFolder
description: Per gli script, ottiene una cartella che contiene le attività in una posizione specificata.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Utilità di pianificazione proprietà GetFolder
- Utilità di pianificazione proprietà GetFolder, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà GetFolder
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
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119291"
---
# <a name="taskfoldergetfolder-property"></a>Proprietà TaskFolder. GetFolder

Per gli script, ottiene una cartella che contiene le attività in una posizione specificata.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valore proprietà

Percorso (percorso) della cartella. Non usare una barra rovesciata che segue il nome dell'ultima cartella nel percorso. La cartella radice dell'attività è specificata con una barra rovesciata ( \) . Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

## <a name="error-codes"></a>Codici di errore

Cartella nel percorso specificato. La cartella è un oggetto [**TaskFolder**](taskfolder.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





