---
title: WeeklyTrigger.WeeksInterval - proprietà
description: Per lo scripting, ottiene o imposta l'intervallo tra le settimane nella pianificazione.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Proprietà WeeksInterval Utilità di pianificazione
- Proprietà WeeksInterval Utilità di pianificazione, oggetto WeeklyTrigger
- Proprietà WeeklyTrigger Utilità di pianificazione , WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080261"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger.WeeksInterval - proprietà

Per lo scripting, ottiene o imposta l'intervallo tra le settimane nella pianificazione.

## <a name="syntax"></a>Sintassi


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valore proprietà

Intervallo tra le settimane nella pianificazione.

## <a name="remarks"></a>Commenti

Un intervallo di 1 produce una pianificazione settimanale. Un intervallo di 2 produce una pianificazione ogni due settimane.

Quando si legge o si scrive codice XML personalizzato per un'attività, l'intervallo per una pianificazione settimanale viene specificato usando l'elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





