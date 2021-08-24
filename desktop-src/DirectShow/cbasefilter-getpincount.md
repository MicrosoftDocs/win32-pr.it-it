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
ms.openlocfilehash: e7d136b5b3bbdcd8a6b21fcbd9f854de7a78a91be87a199c990e294ce8b28fb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640481"
---
# <a name="cbasefiltergetpincount-method"></a>Metodo CBaseFilter.GetPinCount

Il `GetPinCount` metodo recupera il numero di segnaposto.

## <a name="syntax"></a>Sintassi


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il numero di segnaposto.

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo virtuale puro. Restituisce il numero di segnaposto attualmente disponibili in questo filtro. I filtri possono creare o eliminare in modo dinamico i segnaposto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




