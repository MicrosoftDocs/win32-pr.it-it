---
description: Il metodo SetTimeDelta regola l'ora del clock interno.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Metodo CBaseReferenceClock.SetTimeDelta (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9eba5337fa43e43e3b7a45a7a92263fd4e6d69388185a2096c1a270590e482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403440"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Metodo CBaseReferenceClock.SetTimeDelta

Il `SetTimeDelta` metodo regola l'ora del clock interno.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimeDelta* \[ Ref\]
</dt> <dd>

Quantità di regolazione dell'ora dell'orologio, in unità di 100 nanosecondi. Un valore positivo sposta l'orologio in avanti e un valore negativo sposta l'orologio all'indietro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

La classe derivata può usare questo metodo per regolare l'orologio interno, se si allontana dal dispositivo che fornisce informazioni sull'intervallo.

Il [**metodo CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) non restituisce mai valori decrescenti. Se si regola l'orologio all'indietro, **GetTime** restituisce il valore precedente finché l'orologio non raggiunge nuovamente tale valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




