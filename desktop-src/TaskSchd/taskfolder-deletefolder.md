---
title: Metodo TaskFolder.DeleteFolder
description: Per lo scripting, elimina una sottocartella dalla cartella padre.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Metodo DeleteFolder Utilità di pianificazione
- Metodo DeleteFolder Utilità di pianificazione , oggetto TaskFolder
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
ms.openlocfilehash: a73dfe168b599de6e09d5437d0be4ec7a851d246f9fcbce0f79f662b62c56212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974901"
---
# <a name="taskfolderdeletefolder-method"></a>Metodo TaskFolder.DeleteFolder

Per lo scripting, elimina una sottocartella dalla cartella padre.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*folderName* \[ Pollici\]
</dt> <dd>

Nome della sottocartella da rimuovere. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Questo parametro può essere un percorso relativo alla cartella che si vuole eliminare. Un esempio di percorso di cartella di attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Il carattere '.' non può essere usato per specificare la cartella dell'attività corrente e '.'. Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Non supportata.

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

[**Cartella attività**](taskfolder.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





