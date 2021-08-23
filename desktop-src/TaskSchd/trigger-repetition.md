---
title: Trigger.Repetition - proprietà
description: Per lo scripting, ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Proprietà Di ripetizione Utilità di pianificazione
- Proprietà Repetition Utilità di pianificazione, oggetto Trigger
- Attivare l'oggetto Utilità di pianificazione proprietà , Repetition
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e14b8dc23b329d9646647fdcc1c5bcb3166c5bf885886a5308c329e186dc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002109"
---
# <a name="triggerrepetition-property"></a>Trigger.Repetition - proprietà

Per lo scripting, ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

## <a name="syntax"></a>Sintassi


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**RepetitionPattern**](repetitionpattern.md) che definisce la frequenza di esecuzione dell'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML personalizzato per un'attività, il modello di ripetizione per un trigger viene specificato nell'elemento [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) dello schema Utilità di pianificazione dati.

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
</dt> <dt>

[**Pattern ripetizione**](repetitionpattern.md)
</dt> </dl>

 

 





