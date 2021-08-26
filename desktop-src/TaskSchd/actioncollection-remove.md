---
title: Metodo ActionCollection.Remove
description: Per lo scripting, rimuove l'azione specificata dalla raccolta.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Rimuovere il metodo Utilità di pianificazione
- Rimuovere il metodo Utilità di pianificazione, oggetto ActionCollection
- Oggetto ActionCollection Utilità di pianificazione , metodo Remove
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
ms.openlocfilehash: c0c176f41c59bd473e25e82082ada1934a25641e6144f4187e7f25075779b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011741"
---
# <a name="actioncollectionremove-method"></a>Metodo ActionCollection.Remove

Per lo scripting, rimuove l'azione specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

Indice dell'azione da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando si rimuovono elementi, si noti che l'indice per il primo elemento nella raccolta è 1 e l'indice per l'ultimo elemento è il valore [**della proprietà ActionCollection.Count.**](actioncollection-count.md)

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

 

 





