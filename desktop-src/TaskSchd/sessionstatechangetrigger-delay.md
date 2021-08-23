---
title: SessionStateChangeTrigger.Delay - proprietà
description: Per la creazione di script, ottiene o imposta un valore che indica il tempo di ritardo prima dell'avvio di un'attività dopo che è stata rilevata una modifica dello stato della sessione di Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Proprietà Delay Utilità di pianificazione
- Proprietà Delay Utilità di pianificazione , oggetto SessionStateChangeTrigger
- SessionStateChangeTrigger object Utilità di pianificazione , Delay property
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
ms.openlocfilehash: 26767aeca55af5ae208791f42b5973fa38df507a84f08f3d2d1fe8db28965b52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139354"
---
# <a name="sessionstatechangetriggerdelay-property"></a>SessionStateChangeTrigger.Delay - proprietà

Per la creazione di script, ottiene o imposta un valore che indica il tempo di ritardo prima dell'avvio di un'attività dopo che è stata rilevata una modifica dello stato della sessione di Terminal Server. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="syntax"></a>Sintassi


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Ritardo che si verifica prima dell'avvio di un'attività dopo che è stata rilevata una modifica dello stato della sessione di Terminal Server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





