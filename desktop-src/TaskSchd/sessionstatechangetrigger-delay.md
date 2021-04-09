---
title: Proprietà SessionStateChangeTrigger. Delay
description: Per gli script, ottiene o imposta un valore che indica per quanto tempo si verifica un ritardo prima che venga avviata un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto SessionStateChangeTrigger
- Utilità di pianificazione oggetto SessionStateChangeTrigger, proprietà delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119295"
---
# <a name="sessionstatechangetriggerdelay-property"></a>Proprietà SessionStateChangeTrigger. Delay

Per gli script, ottiene o imposta un valore che indica per quanto tempo si verifica un ritardo prima che venga avviata un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="syntax"></a>Sintassi


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Il ritardo che si verifica prima dell'avvio di un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





