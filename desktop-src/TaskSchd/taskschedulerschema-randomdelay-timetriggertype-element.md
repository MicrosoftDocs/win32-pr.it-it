---
title: Elemento RandomDelay (timeTriggerType)
description: Contiene il tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. | Elemento RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Elemento RandomDelay Utilità di pianificazione
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c4c9fde8a0f88ed7e87b5a0d3ccc252f141f6b677f535adf853ef0aca9499b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611507"
---
# <a name="randomdelay-timetriggertype-element"></a>Elemento RandomDelay (timeTriggerType)

Contiene il tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

L'elemento è definito dal [**tipo complesso timeTriggerType.**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                    | Derivato da                                                               | Descrizione                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**TimeTrigger (triggerGroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando il trigger viene attivato.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, [**vedere Proprietà RandomDelay di ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).

Per lo sviluppo di script, [**vedere TimeTrigger.RandomDelay.**](timetrigger-randomdelay.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





