---
title: Proprietà IdleSettings. WaitTimeout
description: Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Utilità di pianificazione proprietà WaitTimeout
- Utilità di pianificazione proprietà WaitTimeout, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, proprietà WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048466"
---
# <a name="idlesettingswaittimeout-property"></a>Proprietà IdleSettings. WaitTimeout

Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività. Se per questa proprietà non viene specificato alcun valore, il servizio Utilità di pianificazione attenderà per un periodo di tempo indefinito che si verifichi una condizione di inattività.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Il tempo minimo consentito è pari a 1 minuto. Se questo valore è **null**, il ritardo verrà impostato sul valore predefinito di 1 ora.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) dello schema utilità di pianificazione.

Se un'attività viene attivata da un trigger inattivo, la proprietà **IdleSettings. WaitTimeout** viene ignorata.

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

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





