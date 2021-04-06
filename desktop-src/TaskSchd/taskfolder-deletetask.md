---
title: TaskFolder. DeleteTask, metodo
description: Per lo scripting, Elimina un'attività dalla cartella.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Utilità di pianificazione del metodo DeleteTask
- Metodo DeleteTask Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742175"
---
# <a name="taskfolderdeletetask-method"></a>TaskFolder. DeleteTask, metodo

Per lo scripting, Elimina un'attività dalla cartella.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome dell'attività specificata quando l'attività è stata registrata. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Non supportata. Il valore è 0

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

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





