---
description: Il metodo IsStopped determina se il filtro contenente questo pin viene arrestato.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Metodo CBasePin.IsStopped (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916391"
---
# <a name="cbasepinisstopped-method"></a>Metodo CBasePin.IsStopped

Il `IsStopped` metodo determina se il filtro contenente questo pin viene arrestato.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il filtro viene arrestato. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Non chiamare questo metodo dall'interno del metodo del costruttore **CBasePin,** perché il filtro potrebbe non essere ancora inizializzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




