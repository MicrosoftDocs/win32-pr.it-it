---
description: Il metodo GetPrivateTime recupera l'ora reale dal clock.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Metodo CBaseReferenceClock. GetPrivateTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332228"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>CBaseReferenceClock. GetPrivateTime, metodo

Il `GetPrivateTime` metodo recupera il tempo reale dal clock.

## <a name="syntax"></a>Sintassi


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce l'ora dell'orologio corrente, in unità di 100 nanosecondi.

## <a name="remarks"></a>Commenti

Questo metodo restituisce il tempo reale segnalato dall'orologio. I chiamanti esterni usano il metodo [**CBaseReferenceClock:: GetTime**](cbasereferenceclock-gettime.md) , che chiama questo metodo. A differenza del metodo **getTime** , il clock interno può tornare indietro. In tal caso, il metodo **getTime** continua a restituire l'ultima volta che ha segnalato, fino a quando il metodo non viene `GetPrivateTime` aggiornato.

Questo metodo restituisce l'ora di sistema. Eseguire l'override di questo metodo se l'orologio ottiene l'ora da un'altra origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




