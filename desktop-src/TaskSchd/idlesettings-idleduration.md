---
title: IdleSettings.IdleDuration - proprietà
description: Per lo scripting, ottiene o imposta un valore che indica la quantità di tempo per cui il computer deve essere inattivo prima dell'esecuzione dell'attività.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Proprietà IdleDuration Utilità di pianificazione
- Proprietà IdleDuration Utilità di pianificazione , oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione , proprietà IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a78210202579d517410a2d82f1c5566d947f1ceb76cbd92538a0266b7b81ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002439"
---
# <a name="idlesettingsidleduration-property"></a>IdleSettings.IdleDuration - proprietà

Per lo scripting, ottiene o imposta un valore che indica la quantità di tempo per cui il computer deve essere inattivo prima dell'esecuzione dell'attività.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica la quantità di tempo per cui il computer deve essere inattivo prima dell'esecuzione dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Il valore minimo è un minuto. Se questo valore è **NULL,** il ritardo verrà impostato sul valore predefinito di 10 minuti.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata [**nell'elemento Duration**](taskschedulerschema-duration-idlesettingstype-element.md) dello schema Utilità di pianificazione attività.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





