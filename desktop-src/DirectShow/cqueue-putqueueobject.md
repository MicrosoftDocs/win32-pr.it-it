---
description: Inserisce un elemento nella coda.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Metodo CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331324"
---
# <a name="cqueueputqueueobject-method"></a>CQueue. PutQueueObject, metodo

Inserisce un elemento nella coda.

## <a name="syntax"></a>Sintassi


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*object* 
</dt> <dd>

Oggetto di tipo **T** (il tipo di modello).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo si blocca fino a quando non è presente spazio nella coda per l'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CQueue**](cqueue.md)
</dt> </dl>

 

 




