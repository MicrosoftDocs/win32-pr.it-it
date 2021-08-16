---
title: Elemento Delay (eventTriggerType)
description: Specifica l'intervallo di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Elemento Delay Utilità di pianificazione
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c9523b450d5f1ea86bdf09afba26604ebfe8055661fc18c439b4e30c97169d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357107"
---
# <a name="delay-eventtriggertype-element"></a>Elemento Delay (eventTriggerType)

Specifica l'intervallo di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**L'elemento Delay** è definito dal [**tipo complesso eventTriggerType.**](taskschedulerschema-eventtriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger di evento viene specificato [**dalla proprietà EventTrigger.Delay.**](eventtrigger-delay.md)

Per lo sviluppo in C++, il ritardo del trigger di evento viene specificato dalla [**proprietà IEventTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





