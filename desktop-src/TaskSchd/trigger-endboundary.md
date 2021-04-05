---
title: Proprietà trigger. EndBoundary
description: Per gli script, ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Utilità di pianificazione proprietà EndBoundary
- Utilità di pianificazione proprietà EndBoundary, oggetto trigger
- Utilità di pianificazione oggetto trigger, proprietà EndBoundary
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
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048146"
---
# <a name="triggerendboundary-property"></a>Proprietà trigger. EndBoundary

Per gli script, ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.

## <a name="syntax"></a>Sintassi


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>Valore proprietà

Data e ora in cui il trigger viene disattivato. Il formato di data e ora deve essere il seguente: AAAA-MM-GGThh: MM: SS (+-) HH: MM. Ad esempio, la data dell'11 ottobre 2005 alle 1:21:17 nel fuso orario del Pacifico viene scritta come 2005-10-11T13:21:17-08:00. La sezione (+-) HH: MM del formato descrive il fuso orario come un determinato numero di ore in anticipo o in base all'ora UTC (ora di Greenwich).

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, la proprietà Enabled viene specificata utilizzando l'elemento [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) dello schema utilità di pianificazione.

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

 

 





