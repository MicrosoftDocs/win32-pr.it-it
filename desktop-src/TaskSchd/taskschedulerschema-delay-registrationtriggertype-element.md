---
title: Elemento Delay (registrationTriggerType)
description: Specifica l'intervallo di tempo tra la registrazione dell'attività e l'avvio dell'attività.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: cd7ba3e9fd0fb71da628ee15bc0f1bdf6281e74ef20f259faf7a5a63504a6f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131850"
---
# <a name="delay-registrationtriggertype-element"></a>Elemento Delay (registrationTriggerType)

Specifica l'intervallo di tempo tra la registrazione dell'attività e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**L'elemento Delay** è definito dal [**tipo complesso registrationTriggerType.**](taskschedulerschema-registrationtriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                     | Derivato da                                                                               | Descrizione                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività viene registrata.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger di registrazione viene specificato usando la [**proprietà RegistrationTrigger.Delay.**](registrationtrigger-delay.md)

Per lo sviluppo in C++, il ritardo del trigger di registrazione viene specificato usando la proprietà [**IRegistrationTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un ritardo del trigger di registrazione che consente un ritardo di 5 minuti tra la registrazione dell'attività e l'avvio dell'attività.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



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

 

 





