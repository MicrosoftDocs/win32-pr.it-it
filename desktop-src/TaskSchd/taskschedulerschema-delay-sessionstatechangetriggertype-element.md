---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contiene un valore che indica la durata del ritardo per un'ora di inizio dell'attività, quando viene rilevata una modifica dello stato della sessione di Terminal Server.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
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
ms.openlocfilehash: 3834b40446509b2b5fe9219947c227a5819e62c1bf398e0ddda7dbb7b4da8ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942809"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>Elemento Delay (sessionStateChangeTriggerType)

Contiene un valore che indica la durata del ritardo per un'ora di inizio dell'attività, quando viene rilevata una modifica dello stato della sessione di Terminal Server. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**L'elemento Delay** è definito dal [**tipo complesso sessionStateChangeTriggerType.**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                       | Derivato da                                                                                           | Descrizione                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando viene modificato lo stato di una sessione di Terminal Server. <br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger di modifica dello stato della sessione viene specificato usando la [**proprietà SessionStateChangeTrigger.Delay.**](sessionstatechangetrigger-delay.md)

Per lo sviluppo in C++, il ritardo del trigger di modifica dello stato della sessione viene specificato usando [**la proprietà Delay di ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





