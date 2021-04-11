---
title: Proprietà trigger. Enabled
description: Per gli script, ottiene o imposta un valore booleano che indica se il trigger è abilitato.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Utilità di pianificazione proprietà abilitata
- Utilità di pianificazione proprietà abilitata, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963980"
---
# <a name="triggerenabled-property"></a>Proprietà trigger. Enabled

Per gli script, ottiene o imposta un valore booleano che indica se il trigger è abilitato.

## <a name="syntax"></a>Sintassi


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Valore proprietà

True se il trigger è abilitato. in caso contrario, false. Il valore predefinito è true.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, la proprietà Enabled viene specificata utilizzando l'elemento [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) dello schema utilità di pianificazione.

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

 

 





