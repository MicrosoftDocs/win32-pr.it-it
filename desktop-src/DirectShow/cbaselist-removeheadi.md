---
description: Il metodo RemoveHeadI rimuove il primo elemento nell'elenco.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Metodo CBaseList.RemoveHeadI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc4d9e039735888d6694422a1802b73b3781316210fd42e13eec9bac5094d322
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814311"
---
# <a name="cbaselistremoveheadi-method"></a>Metodo CBaseList.RemoveHeadI

Il `RemoveHeadI` metodo rimuove il primo elemento nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'elemento oppure **NULL se** l'elenco è vuoto.

## <a name="remarks"></a>Commenti

Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




