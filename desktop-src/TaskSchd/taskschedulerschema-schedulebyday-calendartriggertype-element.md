---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Specifica una pianificazione giornaliera.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- trigger giornaliero Utilità di pianificazione elemento XML
- Elemento ScheduleByDay Utilità di pianificazione
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f29cc4b702ba93aec44e3460279976f50c5563463accfb58b920ad79b757126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131583"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Elemento ScheduleByDay (calendarTriggerType)

Specifica una pianificazione giornaliera. Ad esempio, l'attività inizia alle 8:00 ogni giorno, ogni altro giorno, ogni terzo giorno e così via.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

**L'elemento ScheduleByDay** è definito dal [**tipo complesso calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                             | Derivato da                                                                       | Descrizione                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Specifica un trigger giornaliero, settimanale, mensile o mensile del giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo             | Descrizione                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Specifica l'intervallo tra i giorni nella pianificazione.<br/> |



## <a name="remarks"></a>Commenti

L'elemento figlio elencato in precedenza è definito dai tipi [**di elemento complessi dailyScheduleType.**](taskschedulerschema-dailyscheduletype-complextype.md)

L'ora del giorno in cui l'attività viene avviata viene impostata [**dall'elemento StartBoundary.**](taskschedulerschema-startboundary-triggerbasetype-element.md)

Per lo sviluppo di script, viene specificato un trigger giornaliero usando [**l'oggetto DailyTrigger.**](weeklytrigger.md)

Per lo sviluppo in C++, viene specificato un trigger giornaliero usando [**l'interfaccia IDailyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un trigger di calendario giornaliero che avvia l'attività ogni giorno.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Per un esempio completo del codice XML per un'attività che specifica una pianificazione giornaliera, vedere [Esempio di trigger giornaliero (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





