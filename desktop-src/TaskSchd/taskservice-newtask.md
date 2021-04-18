---
title: TaskService. NewTask, metodo
description: Per lo scripting, restituisce un oggetto di definizione di attività vuoto da compilare con le impostazioni e le proprietà e quindi registrate usando il metodo TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Utilità di pianificazione del metodo NewTask
- Metodo NewTask Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo NewTask
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302670"
---
# <a name="taskservicenewtask-method"></a>TaskService. NewTask, metodo

Per lo scripting, restituisce un oggetto di definizione di attività vuoto da compilare con le impostazioni e le proprietà e quindi registrate usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .

## <a name="syntax"></a>Sintassi


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ in\]
</dt> <dd>

Questo parametro è riservato per utilizzi futuri e deve essere impostato su 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Definizione di attività che specifica tutte le informazioni necessarie per creare una nuova attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





