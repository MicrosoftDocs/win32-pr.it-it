---
description: "Il metodo SetClockDelta regola l'ora dell'orologio. Questo metodo implementa il metodo IAMClockAdjust:: SetClockDelta."
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Metodo CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324467"
---
# <a name="csystemclocksetclockdelta-method"></a>CSystemClock. SetClockDelta, metodo

Il `SetClockDelta` metodo regola l'ora dell'orologio. Questo metodo implementa il metodo [**IAMClockAdjust:: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtDelta* 
</dt> <dd>

Specifica la quantità in base alla quale impostare l'orologio come valore [**di \_ ora di riferimento**](reference-time.md) . Un valore positivo consente di spostare l'orologio avanti e un valore negativo consente di spostare l'orologio indietro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK o un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo chiama semplicemente [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).

I valori dell'ora restituiti da [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) sono a incremento progressivo costante. Se si imposta il clock indietro, **getTime** continua a segnalare l'ora precedente fino a quando l'orologio interno non viene aggiornato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| Intestazione<br/>  | <dl> <dt>Sysclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




