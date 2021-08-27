---
description: Il metodo SetDefaultTimerResolution imposta la risoluzione del timer dell'orologio di riferimento.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Metodo CBaseReferenceClock.SetDefaultTimerResolution (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 980f31856aba14079da0f5b9625dca40846255d6f02361b2798d7c38c1cd4f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087421"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>Metodo CBaseReferenceClock.SetDefaultTimerResolution

Il `SetDefaultTimerResolution` metodo imposta la risoluzione del timer del clock di riferimento.

## <a name="syntax"></a>Sintassi


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*timerResolution* 
</dt> <dd>

Risoluzione minima del timer, in unità da 100 nanosecondi. Se il valore è zero, l'orologio di riferimento annulla la richiesta precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo implementa il [**metodo IReferenceClockTimerControl::SetDefaultTimerResolution.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




