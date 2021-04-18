---
title: Proprietà RepetitionPattern. Duration
description: Per la creazione di script, ottiene o imposta il tempo di ripetizione del modello.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Utilità di pianificazione della proprietà Duration
- Utilità di pianificazione proprietà Duration, oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione, proprietà Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302012"
---
# <a name="repetitionpatternduration-property"></a>Proprietà RepetitionPattern. Duration

Per la creazione di script, ottiene o imposta il tempo di ripetizione del modello.

## <a name="syntax"></a>Sintassi


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>Valore proprietà

Tempo di ripetizione del modello. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Il tempo minimo consentito è di un minuto.

Se non viene specificato alcun valore per la durata, il modello viene ripetuto per un tempo illimitato.

## <a name="remarks"></a>Commenti

Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.

Durante la lettura o la scrittura di codice XML per un'attività, la durata della ripetizione viene specificata nell'elemento [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) dello schema utilità di pianificazione.

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

 

 





