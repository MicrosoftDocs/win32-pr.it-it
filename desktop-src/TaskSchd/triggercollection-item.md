---
title: TriggerCollection.Item - proprietà
description: Per lo scripting, ottiene il trigger specificato dalla raccolta.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Proprietà Item Utilità di pianificazione
- Proprietà Item Utilità di pianificazione, oggetto TriggerCollection
- Oggetto TriggerCollection Utilità di pianificazione proprietà , Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee0460d79ef239c8dacbf7fbd45573dac8ba03ad9b53e6e9881dded1bf01030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001959"
---
# <a name="triggercollectionitem-property"></a>TriggerCollection.Item - proprietà

Per lo scripting, ottiene il trigger specificato dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Trigger**](trigger.md) che rappresenta il trigger richiesto.

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

 

 





