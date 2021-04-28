---
description: 'Metodo CBaseFilter.GetPinCount: il metodo GetPinCount recupera il numero di pin.'
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Metodo CBaseFilter.GetPinCount (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099789"
---
# <a name="cbasefiltergetpincount-method"></a>Metodo CBaseFilter.GetPinCount

Il `GetPinCount` metodo recupera il numero di pin.

## <a name="syntax"></a>Sintassi


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il numero di pin.

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo virtuale puro. Restituisce il numero di pin attualmente disponibili per questo filtro. I filtri possono creare o eliminare in modo dinamico i pin.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




