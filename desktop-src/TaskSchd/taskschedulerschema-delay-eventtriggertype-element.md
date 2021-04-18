---
title: Elemento Delay (eventTriggerType)
description: Specifica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Utilità di pianificazione elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302696"
---
# <a name="delay-eventtriggertype-element"></a>Elemento Delay (eventTriggerType)

Specifica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L'elemento **delay** viene definito dal tipo complesso [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger dell'evento viene specificato dalla proprietà [**EventTrigger. Delay**](eventtrigger-delay.md) .

Per lo sviluppo in C++, il ritardo del trigger dell'evento viene specificato dalla proprietà [**IEventTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





