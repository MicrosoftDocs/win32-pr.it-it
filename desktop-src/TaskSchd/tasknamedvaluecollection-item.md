---
title: TaskNamedValueCollection.Item - proprietà
description: Per lo scripting, ottiene la coppia nome-valore specificata dalla raccolta.
ms.assetid: 89c87b22-e459-435d-8c15-69907e9b1329
keywords:
- Proprietà item Utilità di pianificazione
- Proprietà Item Utilità di pianificazione, oggetto TaskNamedValueCollection
- Oggetto TaskNamedValueCollection Utilità di pianificazione proprietà , Item
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55dd6479486bb481f31e7aaf2b920ef591d1fa1019d432b22568fa7d7f56bf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991471"
---
# <a name="tasknamedvaluecollectionitem-property"></a>TaskNamedValueCollection.Item - proprietà

Per lo scripting, ottiene la coppia nome-valore specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
TaskNamedValueCollection.Item( _
  ByVal index, _
  ByRef pair _
) As long
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**TaskNamedValuePair**](tasknamedvaluepair.md) che rappresenta la coppia richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





