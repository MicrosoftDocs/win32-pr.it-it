---
title: RunningTaskCollection.Item - proprietà
description: Per lo scripting, ottiene l'attività specificata dalla raccolta.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Proprietà item Utilità di pianificazione
- Proprietà Item Utilità di pianificazione , oggetto RunningTaskCollection
- Oggetto RunningTaskCollection Utilità di pianificazione proprietà Item
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
ms.openlocfilehash: a7e2ca7abf5f1daa936509d5fae71211e8b139537fa1782daac6c08bf9a1017f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866781"
---
# <a name="runningtaskcollectionitem-property"></a>RunningTaskCollection.Item - proprietà

Per lo scripting, ottiene l'attività specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**RunningTask**](runningtask.md) che contiene il contesto richiesto.

## <a name="remarks"></a>Commenti

Le raccolte sono basate su 1. In altre parole, l'indice per il primo elemento della raccolta è 1.

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
</dt> </dl>

 

 





