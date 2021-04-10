---
title: Proprietà RunningTaskCollection. Item
description: Per gli script, ottiene l'attività specificata dalla raccolta.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto RunningTaskCollection
- Oggetto RunningTaskCollection Utilità di pianificazione, proprietà Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120418"
---
# <a name="runningtaskcollectionitem-property"></a>Proprietà RunningTaskCollection. Item

Per gli script, ottiene l'attività specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**RunningTask**](runningtask.md) che contiene il contesto richiesto.

## <a name="remarks"></a>Commenti

Le raccolte sono in base 1. In altre parole, l'indice per il primo elemento nella raccolta è 1.

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

 

 





