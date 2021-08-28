---
title: Metodo TaskService.GetFolder
description: Per lo scripting, ottiene una cartella di attività registrate.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Metodo GetFolder Utilità di pianificazione
- Metodo GetFolder Utilità di pianificazione , oggetto TaskService
- Oggetto TaskService Utilità di pianificazione metodo , GetFolder
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
ms.openlocfilehash: 632595e462abd5d6bba5c2e91ebcd590f4ec9a7289092eaf56626e4586691be3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072431"
---
# <a name="taskservicegetfolder-method"></a>Metodo TaskService.GetFolder

Per lo scripting, ottiene una cartella di attività registrate.

## <a name="syntax"></a>Sintassi


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*path* \[ Pollici\]
</dt> <dd>

Percorso della cartella da recuperare. Non usare una barra rovesciata dopo l'ultimo nome di cartella nel percorso. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Un esempio di percorso di cartella di attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Il carattere '.' non può essere usato per specificare la cartella dell'attività corrente e '.'. Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**TaskFolder**](taskfolder.md) per la cartella richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





