---
title: TriggerCollection. Remove (metodo)
description: Per gli script, rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- trigger Utilità di pianificazione, rimozione
- Rimuovere il metodo Utilità di pianificazione
- Rimuovere il metodo Utilità di pianificazione, oggetto TriggerCollection
- TriggerCollection, oggetto Utilità di pianificazione, Remove (metodo)
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
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340612"
---
# <a name="triggercollectionremove-method"></a>TriggerCollection. Remove (metodo)

Per gli script, rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.

## <a name="syntax"></a>Sintassi


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice del trigger da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando si rimuovono elementi, si noti che l'indice per il primo elemento nella raccolta è 1 e l'indice per l'ultimo elemento è il valore della proprietà [**TriggerCollection. Count**](triggercollection-count.md) .

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

 

 





