---
description: Il metodo IncremementPinVersion incrementa il numero di versione nel set di pin.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Metodo CBaseFilter. IncrementPinVersion (Amfilter. h)
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
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331543"
---
# <a name="cbasefilterincrementpinversion-method"></a>CBaseFilter. IncrementPinVersion, metodo

Il `IncremementPinVersion` metodo incrementa il numero di versione nel set di pin.

## <a name="syntax"></a>Sintassi


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa la variabile membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) . Se il filtro crea o Elimina in modo dinamico i pin, chiamare questo metodo ogni volta che i pin cambiano.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




