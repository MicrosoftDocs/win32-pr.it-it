---
title: Elemento Delay (bootTriggerType)
description: Specifica l'intervallo di tempo tra l'avvio del sistema e l'avvio dell'attività.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 91789b22b992af163e9676ef156a2a72f4316ac49b9b47b30ae5599446918bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334601"
---
# <a name="delay-boottriggertype-element"></a>Elemento Delay (bootTriggerType)

Specifica l'intervallo di tempo tra l'avvio del sistema e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**L'elemento Delay** è definito dal [**tipo complesso bootTriggerType.**](taskschedulerschema-boottriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                     | Derivato da                                                               | Descrizione                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) | Specifica un trigger che avvia un'attività all'avvio del sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger di evento viene specificato dalla [**proprietà BootTrigger.Delay.**](boottrigger-delay.md)

Per lo sviluppo in C++, il ritardo del trigger di evento viene specificato dalla proprietà [**IBootTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay)

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

 

 





