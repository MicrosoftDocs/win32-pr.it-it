---
title: Proprietà IdleSettings. StopOnIdleEnd
description: Per la creazione di script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Utilità di pianificazione proprietà StopOnIdleEnd
- Utilità di pianificazione proprietà StopOnIdleEnd, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, proprietà StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873493"
---
# <a name="idlesettingsstoponidleend-property"></a>Proprietà IdleSettings. StopOnIdleEnd

Per la creazione di script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) dello schema utilità di pianificazione.

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

 

 





