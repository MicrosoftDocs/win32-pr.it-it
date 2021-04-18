---
title: EventTrigger. Delay (proprietà)
description: Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, proprietà delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301783"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger. Delay (proprietà)

Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="syntax"></a>Sintassi


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, il ritardo dell'evento viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) dello schema utilità di pianificazione.

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
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





