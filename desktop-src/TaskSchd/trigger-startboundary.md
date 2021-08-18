---
title: Trigger.StartBoundary - proprietà
description: Per lo scripting, ottiene o imposta la data e l'ora di attivazione del trigger.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Proprietà StartBoundary Utilità di pianificazione
- Proprietà StartBoundary Utilità di pianificazione , oggetto Trigger
- Trigger object Utilità di pianificazione , StartBoundary property
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
ms.openlocfilehash: 4b49fa865c215c3190b2d081390c98eec1336ffb00a4bf1e9dd9d94226105e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002079"
---
# <a name="triggerstartboundary-property"></a>Trigger.StartBoundary - proprietà

Per lo scripting, ottiene o imposta la data e l'ora di attivazione del trigger.

## <a name="syntax"></a>Sintassi


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>Valore proprietà

Data e ora di attivazione del trigger. La data e l'ora devono essere nel formato seguente: AAAA-MM-DDTHH:MM:SS(+-)HH:MM. Ad esempio, la data dell'11 ottobre 2005 alle 1:21:17 nel fuso orario del Pacifico verrà scritta come 2005-10-11T13:21:17-08:00. La sezione (+-)HH:MM del formato descrive il fuso orario come un determinato numero di ore avanti o indietro Coordinated Universal Time (ora media di Greenwich).

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, il limite di avvio del trigger viene specificato [**nell'elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) dello schema Utilità di pianificazione attività.

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

 

 





