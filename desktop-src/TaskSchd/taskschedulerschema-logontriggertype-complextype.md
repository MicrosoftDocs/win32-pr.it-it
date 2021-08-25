---
title: Tipo complesso logonTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Tipo complesso logonTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85cbbeaa5d911b1ef9677c79980167a66cdf410c7aa63597b02b007795dfbd81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991212"
---
# <a name="logontriggertype-complex-type"></a>Tipo complesso logonTriggerType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento LogonTrigger.**](taskschedulerschema-logontrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                                                    | Descrizione                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Intervallo di tempo tra l'accesso dell'utente e l'avvio dell'attività.<br/>         |
| [**Userid**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Identificatore dell'utente. L'attività viene avviata quando l'utente accede al computer.<br/> |



## <a name="remarks"></a>Commenti

Oltre agli elementi figlio definiti qui, [**l'elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) usa anche gli elementi figlio definiti dal [**tipo complesso triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





