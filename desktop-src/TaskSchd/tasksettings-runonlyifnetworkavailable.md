---
title: Proprietà TaskSettings. RunOnlyIfNetworkAvailable
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Utilità di pianificazione proprietà RunOnlyIfNetworkAvailable
- Utilità di pianificazione proprietà RunOnlyIfNetworkAvailable, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874289"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Proprietà TaskSettings. RunOnlyIfNetworkAvailable

Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, la proprietà indica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





