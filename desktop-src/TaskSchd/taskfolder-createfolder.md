---
title: Metodo TaskFolder.CreateFolder
description: Per lo scripting, crea una cartella per le attività correlate.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Metodo CreateFolder Utilità di pianificazione
- Metodo CreateFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione , metodo CreateFolder
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
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387079"
---
# <a name="taskfoldercreatefolder-method"></a>Metodo TaskFolder.CreateFolder

Per lo scripting, crea una cartella per le attività correlate.

## <a name="syntax"></a>Sintassi


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*folderName* \[ Pollici\]
</dt> <dd>

Nome utilizzato per identificare la cartella. Se viene specificato \\ "FolderName SubFolder1 SubFolder2", verrà creato l'intero albero di cartelle se \\ le cartelle non esistono. Questo parametro può essere un percorso relativo dell'istanza [**TaskFolder**](taskfolder.md) corrente. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Il carattere '.' non può essere usato per specificare la cartella attività corrente e '..' Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

</dd> <dt>

*sddl* \[ Pollici\]
</dt> <dd>

Descrittore di sicurezza associato alla cartella.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**TaskFolder**](taskfolder.md) che rappresenta la nuova sottocartella.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





