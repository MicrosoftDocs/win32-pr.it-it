---
title: Tipo complesso timeTriggerType
description: Definisce il tipo di base per l'elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Tipo complesso timeTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c03ede1b87f3969d12256df16c0b05c109391876a12c256190966c8befc7f2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355749"
---
# <a name="timetriggertype-complex-type"></a>Tipo complesso timeTriggerType

Definisce il tipo di base per [**l'elemento TimeTrigger.**](taskschedulerschema-timetrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                        | Tipo     | Descrizione                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-timetriggertype-element.md) | duration | Specifica il tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi). <br/> |



## <a name="remarks"></a>Commenti

Si noti che questo elemento non aggiunge elementi figlio a quelli definiti dal tipo complesso [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





