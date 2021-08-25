---
title: ActionCollection.Item - proprietà
description: Per lo scripting, ottiene un'azione specificata dalla raccolta.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Proprietà item Utilità di pianificazione
- Proprietà Item Utilità di pianificazione, oggetto ActionCollection
- Oggetto ActionCollection Utilità di pianificazione proprietà , Item
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
ms.openlocfilehash: fff95b707a4a99ce54cba4d175ce9fd094f7a6bd400147d7942a42a39d65bb7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796641"
---
# <a name="actioncollectionitem-property"></a>ActionCollection.Item - proprietà

Per lo scripting, ottiene un'azione specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Action**](action.md) che rappresenta l'azione richiesta.

## <a name="remarks"></a>Commenti

Le raccolte sono in base 1. In altre parole, l'indice per il primo elemento della raccolta è 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**Actioncollection**](actioncollection.md)
</dt> </dl>

 

 





