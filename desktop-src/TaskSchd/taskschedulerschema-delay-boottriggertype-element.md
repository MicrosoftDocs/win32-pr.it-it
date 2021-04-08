---
title: Elemento Delay (bootTriggerType)
description: Specifica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964957"
---
# <a name="delay-boottriggertype-element"></a>Elemento Delay (bootTriggerType)

Specifica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L'elemento **delay** viene definito dal tipo complesso [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                     | Derivato da                                                               | Descrizione                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando viene avviato il sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger dell'evento viene specificato dalla proprietà [**BootTrigger. Delay**](boottrigger-delay.md) .

Per lo sviluppo in C++, il ritardo del trigger dell'evento viene specificato dalla proprietà [**IBootTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .

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

 

 





