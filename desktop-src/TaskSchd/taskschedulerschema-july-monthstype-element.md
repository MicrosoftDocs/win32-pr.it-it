---
title: Elemento July (monthsType)
description: Specifica che l'attività viene eseguita nel luglio.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Utilità di pianificazione elemento di luglio
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742903"
---
# <a name="july-monthstype-element"></a>Elemento July (monthsType)

Specifica che l'attività viene eseguita nel luglio.

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

L'elemento **July** viene definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                          | Derivato da                                                     | Descrizione                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Mesi (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.<br/> |
| [**Mesi (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.<br/>             |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario dei mesi che esegue l'attività nel mese di luglio.


```XML
<Months>
    <July/>
</Months>
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

 

 





