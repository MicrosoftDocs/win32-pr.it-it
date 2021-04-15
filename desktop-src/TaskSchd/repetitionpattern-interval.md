---
title: Proprietà RepetitionPattern. Interval
description: Per gli script, ottiene o imposta la quantità di tempo che intercorre tra il riavvio dell'attività.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Utilità di pianificazione proprietà intervallo
- Utilità di pianificazione proprietà intervallo, oggetto RepetitionPattern
- Utilità di pianificazione oggetto RepetitionPattern, proprietà Interval
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
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518214"
---
# <a name="repetitionpatterninterval-property"></a>Proprietà RepetitionPattern. Interval

Per gli script, ottiene o imposta la quantità di tempo che intercorre tra il riavvio dell'attività.

## <a name="syntax"></a>Sintassi


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Valore proprietà

Intervallo di tempo tra ogni riavvio dell'attività. Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> (ad esempio, "PT5M" è 5 minuti, "PT1H" è 1 ora e "PT20M" è di 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è pari a 1 minuto.

## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Durante la lettura o la scrittura di codice XML per un'attività, l'intervallo di ripetizione viene specificato nell'elemento [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) dello schema utilità di pianificazione.

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

 

 





