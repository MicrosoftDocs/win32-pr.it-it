---
title: Proprietà ActionCollection. Item
description: Per lo scripting, ottiene un'azione specificata dalla raccolta.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Utilità di pianificazione proprietà elemento
- Utilità di pianificazione proprietà elemento, oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, proprietà Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400801"
---
# <a name="actioncollectionitem-property"></a>Proprietà ActionCollection. Item

Per lo scripting, ottiene un'azione specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**azione**](action.md) che rappresenta l'azione richiesta.

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
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





