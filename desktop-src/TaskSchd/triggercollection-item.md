---
title: Proprietà TriggerCollection. Item
description: Per gli script, ottiene il trigger specificato dalla raccolta.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto TriggerCollection
- TriggerCollection, oggetto Utilità di pianificazione, proprietà Item
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
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740775"
---
# <a name="triggercollectionitem-property"></a>Proprietà TriggerCollection. Item

Per gli script, ottiene il trigger specificato dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**trigger**](trigger.md) che rappresenta il trigger richiesto.

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

 

 





