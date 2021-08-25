---
title: EventTrigger.Delay - proprietà
description: Per lo scripting, ottiene o imposta un valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Proprietà Delay Utilità di pianificazione
- Proprietà Delay Utilità di pianificazione , oggetto EventTrigger
- EventTrigger object Utilità di pianificazione , Delay property
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
ms.openlocfilehash: 402ddb8e55f6eb22a4e2c106b64cbec3ed1afa6d0b58f38a2a8923f5bd8dfa4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959591"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger.Delay - proprietà

Per lo scripting, ottiene o imposta un valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="syntax"></a>Sintassi


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML personalizzato per un'attività, il ritardo dell'evento viene specificato usando l'elemento [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) dello schema Utilità di pianificazione dati.

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
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





