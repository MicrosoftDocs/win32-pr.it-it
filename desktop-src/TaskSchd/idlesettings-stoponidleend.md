---
title: IdleSettings.StopOnIdleEnd - proprietà
description: Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Proprietà StopOnIdleEnd Utilità di pianificazione
- Proprietà StopOnIdleEnd Utilità di pianificazione , oggetto IdleSettings
- Proprietà IdleSettings Utilità di pianificazione , StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e34e95483d382b9fbb97596a7172c94a1a047bfbec0856a3ea17befc1459bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139434"
---
# <a name="idlesettingsstoponidleend-property"></a>IdleSettings.StopOnIdleEnd - proprietà

Per lo scripting, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica che l'Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata [**nell'elemento StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) dello schema Utilità di pianificazione dati.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





