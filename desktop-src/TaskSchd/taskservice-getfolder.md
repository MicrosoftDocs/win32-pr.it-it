---
title: Metodo TaskService. GetFolder
description: Per la creazione di script, ottiene una cartella di attività registrate.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Metodo GetFolder Utilità di pianificazione
- Metodo GetFolder Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302671"
---
# <a name="taskservicegetfolder-method"></a>Metodo TaskService. GetFolder

Per la creazione di script, ottiene una cartella di attività registrate.

## <a name="syntax"></a>Sintassi


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*percorso* \[ in\]
</dt> <dd>

Percorso della cartella da recuperare. Non usare una barra rovesciata che segue il nome dell'ultima cartella nel percorso. La cartella radice dell'attività è specificata con una barra rovesciata ( \) . Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**TaskFolder**](taskfolder.md) per la cartella richiesta.

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

 

 





