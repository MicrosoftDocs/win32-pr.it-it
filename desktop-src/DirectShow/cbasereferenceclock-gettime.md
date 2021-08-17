---
description: Il metodo GetTime recupera l'ora di riferimento corrente. Questo metodo implementa il metodo IReferenceClock::GetTime.
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Metodo CBaseReferenceClock.GetTime (Refclock.h)
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
ms.openlocfilehash: 5a1ffd021ac917a7aa1e12f3d3dc9c4a62ea1f883f126bca1d9c1300d335bdae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954980"
---
# <a name="cbasereferenceclockgettime-method"></a>Metodo CBaseReferenceClock.GetTime

Il `GetTime` metodo recupera l'ora di riferimento corrente. Questo metodo implementa il [**metodo IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)

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

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/>                       |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | L'ora restituita è uguale al valore precedente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>                                         |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) per determinare l'ora reale. Se l'ora dell'orologio è rigorosamente maggiore del valore precedente, usa l'ora `GetTime` dell'orologio e restituisce S \_ OK. In caso `GetTime` contrario, usa il valore precedente e restituisce S \_ FALSE. Pertanto, l'orologio interno può essere eseguito all'indietro per un breve periodo di tempo, senza causare l'esecuzione all'indietro del tempo di riferimento. Al contrario, l'ora di riferimento si "blocca" sullo stesso valore fino a quando il clock interno non si blocca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




