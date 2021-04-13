---
title: Proprietà LogonTrigger. Delay
description: Per lo scripting, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto LogonTrigger
- Utilità di pianificazione oggetto LogonTrigger, proprietà delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400349"
---
# <a name="logontriggerdelay-property"></a>Proprietà LogonTrigger. Delay

Per lo scripting, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.

## <a name="syntax"></a>Sintassi


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il ritardo del trigger LOGON viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-logontriggertype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





