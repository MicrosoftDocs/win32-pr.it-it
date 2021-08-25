---
title: Metodo TaskService.NewTask
description: Per la creazione di script, restituisce un oggetto definizione di attività vuoto da riempire con impostazioni e proprietà e quindi registrato usando il metodo TaskFolder.RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Metodo NewTask Utilità di pianificazione
- Metodo NewTask Utilità di pianificazione , oggetto TaskService
- Oggetto TaskService Utilità di pianificazione metodo , NewTask
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
ms.openlocfilehash: e22da6f62f59bf24ded0eed9dea21e3a1a9d1c3e7ecc36fb6f425f58124aee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990931"
---
# <a name="taskservicenewtask-method"></a>Metodo TaskService.NewTask

Per la creazione di script, restituisce un oggetto definizione di attività vuoto da riempire con le impostazioni e le proprietà e quindi registrato usando il [**metodo TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)

## <a name="syntax"></a>Sintassi


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere impostato su 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Definizione dell'attività che specifica tutte le informazioni necessarie per creare una nuova attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





