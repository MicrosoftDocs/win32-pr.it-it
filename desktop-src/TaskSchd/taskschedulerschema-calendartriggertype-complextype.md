---
title: Tipo complesso calendarTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi del calendario.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Tipo complesso calendarTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a891f60d46f8826faed1cc4b95e4c55f6efa4f7f
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734166"
---
# <a name="calendartriggertype-complex-type"></a>Tipo complesso calendarTriggerType

Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi del calendario.

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                      | Type                                                                                                 | Descrizione                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | duration                                                                                             | Contiene il tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).<br/> |
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Specifica una pianificazione giornaliera. Ad esempio, l'attività inizia ogni giorno, ogni altro giorno, ogni terzo giorno e così via.<br/>                                                                                                               |
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Specifica una pianificazione mensile. Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese in mesi specifici. <br/>                                                                                                       |
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo in base a una pianificazione mensile del giorno della settimana. Ad esempio, l'attività inizia in giorni specifici della settimana, settimane del mese e mesi dell'anno. <br/>                                               |
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Specifica una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni due settimane. <br/>                                                              |



## <a name="remarks"></a>Commenti

Oltre all'elemento figlio definito qui, l'elemento [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) usa anche gli elementi figlio definiti dal tipo complesso [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





