---
description: Il metodo IncremementPinVersion incrementa il numero di versione sul set di pin.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Metodo CBaseFilter.IncrementPinVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01c82a5f506673b6145b468004bbc900d3acdb051f525df20930344137618e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824110"
---
# <a name="cbasefilterincrementpinversion-method"></a>Metodo CBaseFilter.IncrementPinVersion

Il `IncremementPinVersion` metodo incrementa il numero di versione sul set di pin.

## <a name="syntax"></a>Sintassi


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa la [**variabile membro CBaseFilter::m \_ PinVersion.**](cbasefilter-m-pinversion.md) Se il filtro crea o elimina in modo dinamico i pin, chiamare questo metodo ogni volta che i pin cambiano.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




