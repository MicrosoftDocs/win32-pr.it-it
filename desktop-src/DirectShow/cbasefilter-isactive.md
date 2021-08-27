---
description: Il metodo IsActive determina se il filtro è attualmente attivo (in esecuzione o sospeso).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Metodo CBaseFilter.IsActive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbbd9fedf94816d518ef9f8826542399d1d1e97f97137b2d86581d36c4a33e53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076641"
---
# <a name="cbasefilterisactive-method"></a>Metodo CBaseFilter.IsActive

Il `IsActive` metodo determina se il filtro è attualmente attivo (in esecuzione o sospeso).

## <a name="syntax"></a>Sintassi


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il filtro è sospeso o in esecuzione oppure **FALSE** se viene arrestato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




