---
title: Elemento StopAtDurationEnd (repetitionType)
description: Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Utilità di pianificazione elemento StopAtDurationEnd
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302680"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Elemento StopAtDurationEnd (repetitionType)

Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione. Questa operazione è applicabile solo se le ripetizioni sono impostate.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

L'elemento **StopAtDurationEnd** è definito dal tipo complesso [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Elemento padre

| Elemento | Derivato da | Descrizione |
|-|-|-|
| [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |

## <a name="remarks"></a>Commenti

Per lo sviluppo di script, questa impostazione viene specificata tramite la proprietà [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .

Per lo sviluppo in C++, questa impostazione viene specificata tramite la proprietà [**IRepetitionPattern:: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |

## <a name="see-also"></a>Vedi anche

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)

[Utilità di pianificazione](task-scheduler-start-page.md)
