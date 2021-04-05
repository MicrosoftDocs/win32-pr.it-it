---
title: Proprietà BootTrigger. Delay
description: Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto BootTrigger
- Utilità di pianificazione oggetto BootTrigger, proprietà delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120430"
---
# <a name="boottriggerdelay-property"></a>Proprietà BootTrigger. Delay

Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.

## <a name="syntax"></a>Sintassi


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica la quantità di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, il ritardo di avvio viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-boottriggertype-element.md) dello schema utilità di pianificazione.

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

[**BootTrigger**](boottrigger.md)
</dt> </dl>

 

 





