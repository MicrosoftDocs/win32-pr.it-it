---
description: Il metodo arrestato determina se il filtro contenente questo pin è stato arrestato.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Metodo CBasePin. Stopped (Amfilter. h)
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
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332874"
---
# <a name="cbasepinisstopped-method"></a>Metodo CBasePin. Stopped

Il `IsStopped` metodo determina se il filtro contenente questo pin è stato arrestato.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il filtro è arrestato. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Non chiamare questo metodo dall'interno del metodo del costruttore **CBasePin** , perché il filtro potrebbe non essere ancora inizializzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




