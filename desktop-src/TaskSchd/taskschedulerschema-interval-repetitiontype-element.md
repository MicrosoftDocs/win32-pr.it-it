---
title: Elemento Interval (repetitionType)
description: Specifica l'intervallo di tempo tra ogni riavvio dell'attività.
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
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734196"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetitionType)

Specifica l'intervallo di tempo tra ogni riavvio dell'attività. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.

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
| [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**tipo ripetizione**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'intervallo del modello di ripetizione viene specificato usando la [**proprietà RepetitionPattern.Interval.**](repetitionpattern-interval.md)

Per lo sviluppo in C++, l'intervallo del modello di ripetizione viene specificato usando la [**proprietà IRepetitionPattern::Interval.**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un intervallo di ripetizione, vedere [Esempio di trigger giornaliero (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





