---
title: Tipo complesso eventTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Utilità di pianificazione di tipo complesso eventTriggerType
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302168"
---
# <a name="eventtriggertype-complex-type"></a>Tipo complesso eventTriggerType

Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .

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
| [**Abbonamento**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica la query XPath che identifica l'evento che attiva il trigger.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Specifica una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath. Le query vengono applicate a un evento restituito dalla sottoscrizione dell'evento specificato nell'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Il nome del valore della query XPath può essere utilizzato come variabile nell'elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) nella sezione dell'azione [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) di un'attività. <br/> |



## <a name="remarks"></a>Commenti

Oltre all'elemento figlio definito qui, l'elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





