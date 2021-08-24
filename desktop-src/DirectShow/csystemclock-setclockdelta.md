---
description: Il metodo SetClockDelta regola l'ora dell'orologio. Questo metodo implementa il metodo IAMClockAdjust::SetClockDelta.
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Metodo CSystemClock.SetClockDelta (Sysclock.h)
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
ms.openlocfilehash: c98ccf35e41886594a3aab8c3abec6737128d8d7e22f6dfb75d0ac88ac3b7a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538661"
---
# <a name="csystemclocksetclockdelta-method"></a>Metodo CSystemClock.SetClockDelta

Il `SetClockDelta` metodo regola l'ora dell'orologio. Questo metodo implementa il [**metodo IAMClockAdjust::SetClockDelta.**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta)

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

Specifica la quantità in base alla quale regolare l'orologio, come [**valore REFERENCE \_ TIME.**](reference-time.md) Un valore positivo sposta l'orologio in avanti e un valore negativo sposta l'orologio all'indietro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un codice di errore **HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo chiama semplicemente [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).

I valori di ora [**restituiti da IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumentano in modo monotona. Se si imposta nuovamente l'orologio, **GetTime** continua a segnalare l'ora precedente fino al completamento dell'orologio interno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| Intestazione<br/>  | <dl> <dt>Sysclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




