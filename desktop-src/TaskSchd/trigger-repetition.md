---
title: Trigger. proprietà di ripetizione
description: Per lo scripting, ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Utilità di pianificazione della proprietà di ripetizione
- Utilità di pianificazione proprietà di ripetizione, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà di ripetizione
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
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301326"
---
# <a name="triggerrepetition-property"></a>Trigger. proprietà di ripetizione

Per lo scripting, ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

## <a name="syntax"></a>Sintassi


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**RepetitionPattern**](repetitionpattern.md) che definisce la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, il modello di ripetizione per un trigger viene specificato nell'elemento di [**ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) dello schema di utilità di pianificazione.

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
</dt> <dt>

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





