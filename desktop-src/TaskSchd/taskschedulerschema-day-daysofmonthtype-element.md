---
title: Elemento Day (daysOfMonthType)
description: Specifica un giorno del mese durante il quale viene eseguita l'attività.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Elemento Day Utilità di pianificazione
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c238ee5bd873c33f3acd2207ba9ad31869b151924dd20f082669b782d207c59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857954"
---
# <a name="day-daysofmonthtype-element"></a>Elemento Day (daysOfMonthType)

Specifica un giorno del mese durante il quale viene eseguita l'attività.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

**L'elemento** Day è definito dal [**tipo complesso daysOfMonthType.**](taskschedulerschema-daysofmonthtype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                            | Derivato da                                                               | Descrizione                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Specifica i giorni del mese durante i quali viene eseguita l'attività.<br/> |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce la parte relativa ai giorni di un calendario mensile che esegue l'attività il 1° e il 15° giorno del mese.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





