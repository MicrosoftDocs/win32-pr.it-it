---
title: Elemento Interval (repetitionType)
description: Specifica la quantità di tempo tra ogni riavvio dell'attività.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Elemento Interval Utilità di pianificazione
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec6f2724f4374ed94fff47e6577a2887ca953cae0af66de9c64971cd80aa2050
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100001"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetitionType)

Specifica la quantità di tempo tra ogni riavvio dell'attività. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dal tipo [**complesso repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                      | Derivato da                                                             | Descrizione                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'avvio dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'intervallo del criterio di ripetizione viene specificato usando la [**proprietà RepetitionPattern.Interval.**](repetitionpattern-interval.md)

Per lo sviluppo C++, l'intervallo del modello di ripetizione viene specificato usando la [**proprietà IRepetitionPattern::Interval.**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un intervallo di ripetizione, vedere [Daily Trigger Example (XML) ( Esempio di trigger giornaliero (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





