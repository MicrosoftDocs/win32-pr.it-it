---
title: Metodo TaskFolder.CreateFolder
description: Per lo scripting, crea una cartella per le attività correlate.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Metodo CreateFolder Utilità di pianificazione
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
ms.openlocfilehash: 2a5de913ccf98ee8369430425e423813168c083cbde737b5831917a5ee594e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759021"
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

Nome utilizzato per identificare la cartella. Se viene specificato \\ "FolderName SubFolder1 SubFolder2", verrà creato l'intero albero di cartelle se \\ le cartelle non esistono. Questo parametro può essere un percorso relativo dell'istanza [**TaskFolder**](taskfolder.md) corrente. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Non è possibile usare il carattere '.' per specificare la cartella attività corrente e '..' Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





