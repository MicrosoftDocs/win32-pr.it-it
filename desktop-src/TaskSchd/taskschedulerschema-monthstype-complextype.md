---
title: Tipo complesso monthsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi months (monthlyDayOfWeekScheduleType) e months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- Utilità di pianificazione di tipo complesso monthsType
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740439"
---
# <a name="monthstype-complex-type"></a>Tipo complesso monthsType

Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) e [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo | Descrizione                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**Aprile**](taskschedulerschema-april-monthstype-element.md)         | N/D  | Specifica che l'attività viene eseguita nell'aprile. <br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       | N/D  | Specifica che l'attività viene eseguita nell'agosto. <br/>    |
| [**Dicembre**](taskschedulerschema-december-monthstype-element.md)   | N/D  | Specifica che l'attività viene eseguita nel dicembre. <br/>  |
| [**Febbraio**](taskschedulerschema-february-monthstype-element.md)   | N/D  | Specifica che l'attività viene eseguita nel febbraio. <br/>  |
| [**Gennaio**](taskschedulerschema-january-monthstype-element.md)     | N/D  | Specifica che l'attività viene eseguita nel gennaio. <br/>   |
| [**Luglio**](taskschedulerschema-july-monthstype-element.md)           | N/D  | Specifica che l'attività viene eseguita nel luglio. <br/>      |
| [**Giugno**](taskschedulerschema-june-monthstype-element.md)           | N/D  | Specifica che l'attività viene eseguita in giugno. <br/>      |
| [**Marzo**](taskschedulerschema-march-monthstype-element.md)         | N/D  | Specifica che l'attività viene eseguita nel marzo. <br/>     |
| [**Mag**](taskschedulerschema-may-monthstype-element.md)             | N/D  | Specifica che l'attività viene eseguita in May. <br/>       |
| [**Novembre**](taskschedulerschema-november-monthstype-element.md)   | N/D  | Specifica che l'attività viene eseguita nel novembre. <br/>  |
| [**Ottobre**](taskschedulerschema-october-monthstype-element.md)     | N/D  | Specifica che l'attività viene eseguita nel ottobre. <br/>   |
| [**Settembre**](taskschedulerschema-september-monthstype-element.md) | N/D  | Specifica che l'attività viene eseguita nel settembre. <br/> |



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

 

 





