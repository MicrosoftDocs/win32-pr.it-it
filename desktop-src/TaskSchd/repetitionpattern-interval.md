---
title: Proprietà RepetitionPattern.Interval
description: Per lo scripting, ottiene o imposta la quantità di tempo tra ogni riavvio dell'attività.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Proprietà Interval Utilità di pianificazione
- Proprietà Interval Utilità di pianificazione, oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione proprietà Interval
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
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734176"
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

Durante la lettura o la scrittura di codice XML per un'attività, l'intervallo di ripetizione viene specificato [**nell'elemento Interval**](taskschedulerschema-interval-repetitiontype-element.md) dello schema Utilità di pianificazione attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





