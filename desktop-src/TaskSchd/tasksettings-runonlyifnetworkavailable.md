---
title: TaskSettings.RunOnlyIfNetworkAvailable - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Proprietà RunOnlyIfNetworkAvailable Utilità di pianificazione
- Proprietà RunOnlyIfNetworkAvailable Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193d235276ffc37513c95b5ae0a4cef5a6e84cd0bc7d8bea7fab67a262110080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354848"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>TaskSettings.RunOnlyIfNetworkAvailable - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se True, la proprietà indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) dello schema Utilità di pianificazione dati.

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

 

 





