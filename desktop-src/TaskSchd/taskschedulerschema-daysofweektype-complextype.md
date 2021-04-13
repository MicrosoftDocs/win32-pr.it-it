---
title: Tipo complesso daysOfWeekType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi DaysOfWeek (weeklyScheduleType) e DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- Utilità di pianificazione di tipo complesso daysOfWeekType
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341333"
---
# <a name="daysofweektype-complex-type"></a>Tipo complesso daysOfWeekType

Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) e [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                   | Tipo | Descrizione                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**Friday**](taskschedulerschema-friday-daysofweektype-element.md)       | N/D  | L'attività viene eseguita il venerdì. <br/>    |
| [**Monday**](taskschedulerschema-monday-daysofweektype-element.md)       | N/D  | L'attività viene eseguita il lunedì.<br/>     |
| [**Sabato**](taskschedulerschema-saturday-daysofweektype-element.md)   | N/D  | L'attività viene eseguita il sabato. <br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       | N/D  | L'attività viene eseguita la domenica. <br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   | N/D  | Attività eseguita il giovedì <br/>   |
| [**Tuesday**](taskschedulerschema-tuesday-daysofweektype-element.md)     | N/D  | L'attività viene eseguita il martedì. <br/>   |
| [**Wednesday**](taskschedulerschema-wednesday-daysofweektype-element.md) | N/D  | L'attività viene eseguita il mercoledì. <br/> |



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

 

 





