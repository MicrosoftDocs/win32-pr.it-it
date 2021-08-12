---
title: Tipo complesso eventTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Tipo complesso eventTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0acd4bafa6033e461b69180862a8302e76f363b581d7f06b0812824f2031780b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612054"
---
# <a name="eventtriggertype-complex-type"></a>Tipo complesso eventTriggerType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento EventTrigger.**](taskschedulerschema-eventtrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | Specifica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica la query XPath che identifica l'evento che attiva il trigger.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Specifica una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath. Le query vengono applicate a un evento restituito dalla sottoscrizione di eventi specificata [**nell'elemento Subscription.**](taskschedulerschema-subscription-eventtriggertype-element.md) Il nome del valore della query XPath può essere usato come variabile nell'elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) della [**sezione dell'azione ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) di un'attività. <br/> |



## <a name="remarks"></a>Commenti

Oltre all'elemento figlio definito qui, [**l'elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) usa anche gli elementi figlio definiti dal tipo complesso [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

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

 

 





