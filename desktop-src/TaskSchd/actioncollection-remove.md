---
title: Metodo ActionCollection. Remove
description: Per la creazione di script, rimuove l'azione specificata dalla raccolta.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Rimuovere il metodo Utilità di pianificazione
- Remove Method Utilità di pianificazione, oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, metodo Remove
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742463"
---
# <a name="actioncollectionremove-method"></a>Metodo ActionCollection. Remove

Per la creazione di script, rimuove l'azione specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice dell'azione da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando si rimuovono elementi, si noti che l'indice per il primo elemento nella raccolta è 1 e l'indice per l'ultimo elemento è il valore della proprietà [**ActionCollection. Count**](actioncollection-count.md) .

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

 

 





