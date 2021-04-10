---
title: Months (monthlyScheduleType)-elemento
description: Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Utilità di pianificazione dell'elemento months
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120898"
---
# <a name="months-monthlyscheduletype-element"></a>Months (monthlyScheduleType)-elemento

Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

L'elemento **months** viene definito dal tipo complesso [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                    | Derivato da                                                                       | Descrizione                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) | Specifica una pianificazione mensile. <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo | Descrizione                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Aprile (monthsType)**](taskschedulerschema-april-monthstype-element.md)         |      | Specifica che l'attività viene eseguita nell'aprile.<br/>     |
| [**Agosto (monthsType)**](taskschedulerschema-august-monthstype-element.md)       |      | Specifica che l'attività viene eseguita nell'agosto.<br/>    |
| [**Dicembre (monthsType)**](taskschedulerschema-december-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel dicembre.<br/>  |
| [**Febbraio (monthsType)**](taskschedulerschema-february-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel febbraio.<br/>  |
| [**Gennaio (monthsType)**](taskschedulerschema-january-monthstype-element.md)     |      | Specifica che l'attività viene eseguita nel gennaio.<br/>   |
| [**Luglio (monthsType)**](taskschedulerschema-july-monthstype-element.md)           |      | Specifica che l'attività viene eseguita nel luglio.<br/>      |
| [**Giugno (monthsType)**](taskschedulerschema-june-monthstype-element.md)           |      | Specifica che l'attività viene eseguita in giugno.<br/>      |
| [**Marzo (monthsType)**](taskschedulerschema-march-monthstype-element.md)         |      | Specifica che l'attività viene eseguita nel marzo.<br/>     |
| [**Maggio (monthsType)**](taskschedulerschema-may-monthstype-element.md)             |      | Specifica che l'attività viene eseguita in May.<br/>       |
| [**Novembre (monthsType)**](taskschedulerschema-november-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel novembre.<br/>  |
| [**Ottobre (monthsType)**](taskschedulerschema-october-monthstype-element.md)     |      | Specifica che l'attività viene eseguita nel ottobre.<br/>   |
| [**Settembre (monthsType)**](taskschedulerschema-september-monthstype-element.md) |      | Specifica che l'attività viene eseguita nel settembre.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, i mesi della pianificazione vengono specificati utilizzando la proprietà [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .

Per lo sviluppo in C++, i mesi della pianificazione vengono specificati utilizzando la proprietà [**IMonthlyTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario mensile che avvia l'attività il primo e il quindicesimo giorno di ogni mese dell'anno.


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





