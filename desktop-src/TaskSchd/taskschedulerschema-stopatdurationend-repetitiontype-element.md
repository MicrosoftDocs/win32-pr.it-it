---
title: Elemento StopAtDurationEnd (repetitionType)
description: Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Elemento StopAtDurationEnd Utilità di pianificazione
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 896aa6db4ce5bf2c0dddf666024c143754afc97ec76bfb557e6431f593689857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010541"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Elemento StopAtDurationEnd (repetitionType)

Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione. Questa opzione è applicabile solo se sono impostate ripetizioni.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

**L'elemento StopAtDurationEnd** è definito dal tipo [**complesso repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)

## <a name="parent-element"></a>Elemento padre

| Elemento | Derivato da | Descrizione |
|-|-|-|
| [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**tipo di ripetizione**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |

## <a name="remarks"></a>Commenti

Per lo sviluppo di script, questa impostazione viene specificata usando la [**proprietà RepetitionPattern.StopAtDurationEnd.**](repetitionpattern-stopatdurationend.md)

Per lo sviluppo in C++, questa impostazione viene specificata usando la [**proprietà IRepetitionPattern::StopAtDurationEnd.**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |

## <a name="see-also"></a>Vedi anche

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)

[Utilità di pianificazione](task-scheduler-start-page.md)
