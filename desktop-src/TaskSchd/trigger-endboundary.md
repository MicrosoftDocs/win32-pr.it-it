---
title: Trigger.EndBoundary - proprietà
description: Per lo scripting, ottiene o imposta la data e l'ora in cui il trigger viene disattivato. Il trigger non può avviare l'attività dopo che è stata disattivata.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Proprietà EndBoundary Utilità di pianificazione
- Proprietà EndBoundary Utilità di pianificazione, oggetto Trigger
- Attivare l'Utilità di pianificazione, proprietà EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4f2b72100a7b981246788b38572c014a722c126115ab5a77d77eb7d96273f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010451"
---
# <a name="triggerendboundary-property"></a>Trigger.EndBoundary - proprietà

Per lo scripting, ottiene o imposta la data e l'ora in cui il trigger viene disattivato. Il trigger non può avviare l'attività dopo che è stata disattivata.

## <a name="syntax"></a>Sintassi


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valore proprietà

Data e ora di disattivazione del trigger. La data e l'ora devono essere nel formato seguente: AAAA-MM-GGGGHH:MM:SS(+-)HH:MM. Ad esempio, la data dell'11 ottobre 2005 alle 13:21:17 nel fuso orario del Pacifico verrà scritta come 2005-10-11T13:21:17-08:00. La sezione (+-)HH:MM del formato descrive il fuso orario come un determinato numero di ore avanti o indietro Coordinated Universal Time (ora di Greenwich).

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, la proprietà enabled viene specificata usando [**l'elemento EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





