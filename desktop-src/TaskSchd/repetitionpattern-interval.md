---
title: Proprietà RepetitionPattern.Interval
description: Per lo scripting, ottiene o imposta la quantità di tempo tra ogni riavvio dell'attività.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Proprietà Interval Utilità di pianificazione
- Proprietà Interval Utilità di pianificazione , oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione , proprietà Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6efcaa56d2c251b5e044c87091bc646c21f8691aa384ad522b6062014fd496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072621"
---
# <a name="repetitionpatterninterval-property"></a>Proprietà RepetitionPattern.Interval

Per lo scripting, ottiene o imposta la quantità di tempo tra ogni riavvio dell'attività.

## <a name="syntax"></a>Sintassi


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Valore proprietà

Intervallo di tempo tra ogni riavvio dell'attività. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.

## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Quando si legge o si scrive codice XML per un'attività, l'intervallo di ripetizione viene specificato nell'elemento [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) dello schema Utilità di pianificazione schema.

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

 

 





