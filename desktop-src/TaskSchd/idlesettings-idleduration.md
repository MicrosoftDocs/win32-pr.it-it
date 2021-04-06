---
title: Proprietà IdleSettings. IdleDuration
description: Per gli script, ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Utilità di pianificazione proprietà IdleDuration
- Utilità di pianificazione proprietà IdleDuration, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, Proprietà IdleDuration
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
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742455"
---
# <a name="idlesettingsidleduration-property"></a>Proprietà IdleSettings. IdleDuration

Per gli script, ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Valore proprietà

Valore che indica la quantità di tempo in cui il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Il valore minimo è di un minuto. Se questo valore è **null**, il ritardo verrà impostato sul valore predefinito di 10 minuti.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) dello schema utilità di pianificazione.

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

 

 





