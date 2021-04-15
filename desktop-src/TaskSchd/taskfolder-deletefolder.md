---
title: TaskFolder. DeleteFolder, metodo
description: Per la creazione di script, Elimina una sottocartella dalla cartella padre.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Utilità di pianificazione del metodo DeleteFolder
- Metodo DeleteFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477482"
---
# <a name="taskfolderdeletefolder-method"></a>TaskFolder. DeleteFolder, metodo

Per la creazione di script, Elimina una sottocartella dalla cartella padre.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cartellaname* \[ in\]
</dt> <dd>

Nome della sottocartella da rimuovere. La cartella radice dell'attività è specificata con una barra rovesciata ( \) . Questo parametro può essere un percorso relativo della cartella che si desidera eliminare. Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Non supportata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





