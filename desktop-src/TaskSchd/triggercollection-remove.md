---
title: Metodo TriggerCollection.Remove
description: Per lo scripting, rimuove il trigger specificato dalla raccolta di trigger usati dall'attività.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- trigger Utilità di pianificazione , rimozione
- Rimuovere il metodo Utilità di pianificazione
- Rimuovere il metodo Utilità di pianificazione, oggetto TriggerCollection
- Oggetto TriggerCollection Utilità di pianificazione, metodo Remove
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ff3fda5119f4b487ba7f04546ea94e0a601a4749e1aa6aad7a9120907cd6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099646"
---
# <a name="triggercollectionremove-method"></a>Metodo TriggerCollection.Remove

Per lo scripting, rimuove il trigger specificato dalla raccolta di trigger usati dall'attività.

## <a name="syntax"></a>Sintassi


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

Indice del trigger da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando si rimuovono elementi, si noti che l'indice per il primo elemento della raccolta è 1 e l'indice per l'ultimo elemento è il valore [**della proprietà TriggerCollection.Count.**](triggercollection-count.md)

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
</dt> </dl>

 

 





