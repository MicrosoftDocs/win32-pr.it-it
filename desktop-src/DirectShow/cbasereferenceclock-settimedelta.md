---
description: Il metodo SetTimeDelta regola l'ora di clock interna.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Metodo CBaseReferenceClock. SetTimeDelta (Refclock. h)
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
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332220"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>CBaseReferenceClock. SetTimeDelta, metodo

Il `SetTimeDelta` metodo regola l'ora di clock interna.

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

Valore che consente di regolare l'ora di clock, in unità di 100 nanosecondi. Un valore positivo consente di spostare l'orologio avanti e un valore negativo consente di spostare l'orologio indietro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

La classe derivata può utilizzare questo metodo per modificare il clock interno, se deriva dal dispositivo che fornisce informazioni sulla tempistica.

Il metodo [**CBaseReferenceClock:: GetTime**](cbasereferenceclock-gettime.md) restituisce mai valori decrescenti. Se si imposta l'orologio indietro, **getTime** restituisce il valore precedente fino a quando l'orologio raggiunge nuovamente tale valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




