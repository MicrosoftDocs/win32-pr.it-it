---
description: Il metodo GetPinCount Recupera il numero di pin.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Metodo CBaseFilter. GetPinCount (Amfilter. h)
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331553"
---
# <a name="cbasefiltergetpincount-method"></a>CBaseFilter. GetPinCount, metodo

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

La classe derivata deve implementare questo metodo virtuale puro. Restituisce il numero di PIN attualmente disponibili in questo filtro. I filtri possono creare o eliminare in modo dinamico i pin.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




