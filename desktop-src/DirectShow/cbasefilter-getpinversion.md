---
description: Il metodo GetPinVersion recupera un numero di versione per il set di segnaposto in questo filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Metodo CBaseFilter.GetPinVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40890ce40e75ebea9f7dd10edb78572eb865ea5f94cd1ec674c082d6df8c631
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640461"
---
# <a name="cbasefiltergetpinversion-method"></a>Metodo CBaseFilter.GetPinVersion

Il `GetPinVersion` metodo recupera un numero di versione per il set di segnaposto in questo filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la [**variabile membro CBaseFilter::m \_ PinVersion.**](cbasefilter-m-pinversion.md)

## <a name="remarks"></a>Commenti

Il **costruttore CBaseFilter** inizializza la versione del pin su 1. Nella classe di base questo numero non cambia mai. Se il filtro crea o elimina in modo dinamico i segnaposto, deve incrementare la versione del pin ogni volta che i pin cambiano. Per incrementare il numero di versione, chiamare [**il metodo CBaseFilter::IncrementPinVersion.**](cbasefilter-incrementpinversion.md)

L'oggetto enumeratore pin, implementato dalla [**classe CEnumPins,**](cenumpins.md) usa la versione del pin per mantenersi sincronizzato con il filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




