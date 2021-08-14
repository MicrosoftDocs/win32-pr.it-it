---
title: Metodo TaskFolder.DeleteTask
description: Per lo scripting, elimina un'attività dalla cartella.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Metodo DeleteTask Utilità di pianificazione
- Metodo DeleteTask Utilità di pianificazione , oggetto TaskFolder
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
ms.openlocfilehash: c12b3ca9d66817972d75bd3ffbab61bcdcdff5dcc227e680ed6548f77d1b0de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402401"
---
# <a name="taskfolderdeletetask-method"></a>Metodo TaskFolder.DeleteTask

Per lo scripting, elimina un'attività dalla cartella.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Nome dell'attività specificato al momento della registrazione dell'attività. Il carattere '.' non può essere usato per specificare la cartella dell'attività corrente e '.'. Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Non supportata. Il valore è 0

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

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

 

 





