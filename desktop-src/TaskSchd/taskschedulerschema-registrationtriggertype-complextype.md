---
title: Tipo complesso registrationTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- Tipo complesso registrationTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dab91ecc0eed065a4ce3eea9d64bebae2e10560a43ab57308ea68e82dc17dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772281"
---
# <a name="registrationtriggertype-complex-type"></a>Tipo complesso registrationTriggerType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento RegistrationTrigger.**](taskschedulerschema-registrationtrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
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



| Elemento                                                                    | Tipo     | Descrizione                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | Specifica l'intervallo di tempo tra la registrazione dell'attività e l'avvio dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Oltre agli elementi figlio definiti qui, [**l'elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) usa anche gli elementi figlio definiti dal [**tipo complesso triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

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

 

 





