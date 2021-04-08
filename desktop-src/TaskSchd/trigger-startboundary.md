---
title: Proprietà trigger. StartBoundary
description: Per gli script, ottiene o imposta la data e l'ora di attivazione del trigger.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Utilità di pianificazione proprietà StartBoundary
- Utilità di pianificazione proprietà StartBoundary, oggetto trigger
- Utilità di pianificazione oggetto trigger, proprietà StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740794"
---
# <a name="triggerstartboundary-property"></a>Proprietà trigger. StartBoundary

Per gli script, ottiene o imposta la data e l'ora di attivazione del trigger.

## <a name="syntax"></a>Sintassi


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Valore proprietà

Data e ora di attivazione del trigger. Il formato di data e ora deve essere il seguente: AAAA-MM-GGThh: MM: SS (+-) HH: MM. Ad esempio, la data dell'11 ottobre 2005 alle 1:21:17 nel fuso orario del Pacifico viene scritta come 2005-10-11T13:21:17-08:00. La sezione (+-) HH: MM del formato descrive il fuso orario come un determinato numero di ore in anticipo o in base all'ora UTC (ora di Greenwich).

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il limite di avvio del trigger viene specificato nell'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





