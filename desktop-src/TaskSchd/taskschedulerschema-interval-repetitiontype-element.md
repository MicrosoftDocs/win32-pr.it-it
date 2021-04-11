---
title: Elemento Interval (repetitionType)
description: Specifica la quantità di tempo tra ogni riavvio dell'attività.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Utilità di pianificazione dell'elemento Interval
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963985"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetitionType)

Specifica la quantità di tempo tra ogni riavvio dell'attività. Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> (ad esempio, "PT5M" è 5 minuti, "PT1H" è 1 ora e "PT20M" è di 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è pari a 1 minuto.

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

L'elemento è definito dal tipo complesso [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                      | Derivato da                                                             | Descrizione                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'intervallo del modello di ripetizione viene specificato utilizzando la proprietà [**RepetitionPattern. Interval**](repetitionpattern-interval.md) .

Per lo sviluppo in C++, l'intervallo del modello di ripetizione viene specificato tramite la proprietà [**IRepetitionPattern:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un intervallo di ripetizione, vedere [esempio di trigger giornalieri (XML)](daily-trigger-example--xml-.md).

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

 

 





