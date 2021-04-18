---
title: TaskFolder. CreateFolder, metodo
description: Per gli script, crea una cartella per le attività correlate.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Utilità di pianificazione del metodo CreateFolder
- Metodo CreateFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301910"
---
# <a name="taskfoldercreatefolder-method"></a>TaskFolder. CreateFolder, metodo

Per gli script, crea una cartella per le attività correlate.

## <a name="syntax"></a>Sintassi


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cartellaname* \[ in\]
</dt> <dd>

Nome utilizzato per identificare la cartella. Se si specifica "FolderName \\ Sottocartella1 \\ SubFolder2", verrà creato l'intero albero delle cartelle se le cartelle non esistono. Questo parametro può essere un percorso relativo dell'istanza corrente di [**TaskFolder**](taskfolder.md) . La cartella radice dell'attività è specificata con una barra rovesciata ( \) . Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

</dd> <dt>

*SDDL* \[ in\]
</dt> <dd>

Descrittore di sicurezza associato alla cartella.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**TaskFolder**](taskfolder.md) che rappresenta la nuova sottocartella.

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
</dt> </dl>

 

 





