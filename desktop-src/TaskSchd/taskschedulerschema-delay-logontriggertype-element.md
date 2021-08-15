---
title: Elemento Delay (logonTriggerType)
description: Intervallo di tempo tra l'accesso dell'utente e l'avvio dell'attività.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Ritardo dell'Utilità di pianificazione
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bd18652630ad14f9b888db6a810d8da1eb42a18fb9d2caa6726414aa9054702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357138"
---
# <a name="delay-logontriggertype-element"></a>Elemento Delay (logonTriggerType)

Intervallo di tempo tra l'accesso dell'utente e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**L'elemento Delay** è definito dal tipo complesso [**logonTriggerType.**](taskschedulerschema-logontriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando un utente accede.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger di accesso viene specificato tramite la [**proprietà LogonTrigger.Delay.**](logontrigger-delay.md)

Per lo sviluppo C++, l'identificatore utente per il trigger di accesso viene specificato usando la proprietà [**ILogonTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





