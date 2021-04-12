---
title: Tipo complesso bootTriggerType
description: Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Utilità di pianificazione di tipo complesso bootTriggerType
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478191"
---
# <a name="boottriggertype-complex-type"></a>Tipo complesso bootTriggerType

Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="bootTriggerType">
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



| Elemento                                                            | Tipo     | Descrizione                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-boottriggertype-element.md) | duration | Intervallo di tempo tra il momento in cui il sistema viene avviato e il momento in cui viene attivato il trigger. <br/> |



## <a name="remarks"></a>Commenti

Oltre all'elemento figlio definito qui, l'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





