---
title: Elemento Day (daysOfMonthType)
description: Specifica un giorno del mese durante il quale viene eseguita l'attività.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Utilità di pianificazione elemento Day
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048092"
---
# <a name="day-daysofmonthtype-element"></a>Elemento Day (daysOfMonthType)

Specifica un giorno del mese durante il quale viene eseguita l'attività.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

L'elemento **Day** è definito dal tipo complesso [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                            | Derivato da                                                               | Descrizione                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Specifica i giorni del mese durante i quali viene eseguita l'attività.<br/> |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce la parte relativa ai giorni di un calendario mensile che esegue l'attività il primo e il quindicesimo giorno del mese.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





