---
description: Recupera l'elemento successivo dalla coda.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Metodo CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331326"
---
# <a name="cqueuegetqueueobject-method"></a>CQueue. GetQueueObject, metodo

Recupera l'elemento successivo dalla coda.

## <a name="syntax"></a>Sintassi


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un oggetto di tipo **T** (il tipo di modello).

## <a name="remarks"></a>Commenti

Questo metodo si blocca fino a quando un elemento non è disponibile nella coda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CQueue**](cqueue.md)
</dt> </dl>

 

 




