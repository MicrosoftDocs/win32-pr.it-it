---
description: "Il metodo getTime recupera l'ora di riferimento corrente. Questo metodo implementa il metodo IReferenceClock:: GetTime."
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Metodo CBaseReferenceClock. getTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332227"
---
# <a name="cbasereferenceclockgettime-method"></a>CBaseReferenceClock. getTime, metodo

Il `GetTime` metodo recupera l'ora di riferimento corrente. Questo metodo implementa il metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora corrente, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/>                       |
| <dl> <dt>**S \_ false**</dt> </dl>   | L'ora restituita è uguale a quella del valore precedente.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                                         |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) per determinare l'ora reale del clock. Se l'ora dell'orologio è rigorosamente maggiore del valore precedente, `GetTime` Usa l'ora di clock e restituisce \_ OK. In caso contrario, `GetTime` Usa il valore precedente e restituisce \_ false. Pertanto, il clock interno può essere eseguito all'indietro per un breve periodo di tempo, senza comportare l'esecuzione precedente dell'ora di riferimento. Al contrario, l'ora di riferimento si "blocca" con lo stesso valore fino a quando l'orologio interno non viene ripreso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




