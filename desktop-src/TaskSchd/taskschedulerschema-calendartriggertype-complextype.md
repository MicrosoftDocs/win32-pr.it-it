---
title: Tipo complesso calendarTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi del calendario.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Utilità di pianificazione di tipo complesso calendarTriggerType
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302005"
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



| Elemento                                                                                                      | Tipo                                                                                                 | Descrizione                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | duration                                                                                             | Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> S (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).<br/> |
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Specifica una pianificazione giornaliera. Ad esempio, l'attività viene avviata ogni giorno, ogni giorno, ogni tre giorni e così via.<br/>                                                                                                               |
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Specifica una pianificazione mensile. Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese per mesi specifici. <br/>                                                                                                       |
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo in base a una pianificazione mensile del giorno della settimana. Ad esempio, l'attività viene avviata in giorni specifici della settimana, settimane del mese e mesi dell'anno. <br/>                                               |
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Specifica una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni altra settimana. <br/>                                                              |



## <a name="remarks"></a>Commenti

Oltre all'elemento figlio definito qui, l'elemento [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) usa anche gli elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





