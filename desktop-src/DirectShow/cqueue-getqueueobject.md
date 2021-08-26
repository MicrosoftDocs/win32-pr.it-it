---
description: Recupera l'elemento successivo dalla coda.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Metodo CQueue.GetQueueObject (Wxutil.h)
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
ms.openlocfilehash: 6c32039a82e3a0b5c086cbe18e895bdec1aaac09d4947b90d9ba18e8c6636d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108281"
---
# <a name="cqueuegetqueueobject-method"></a>Metodo CQueue.GetQueueObject

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
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CQueue**](cqueue.md)
</dt> </dl>

 

 




