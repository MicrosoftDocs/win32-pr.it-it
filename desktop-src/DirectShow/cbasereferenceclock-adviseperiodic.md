---
description: Il metodo AdvisePeriodic crea una richiesta di consulenza periodica. Questo metodo implementa il metodo IReferenceClock::AdvisePeriodic.
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Metodo CBaseReferenceClock.AdvisePeriodic (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4b81fc8dfc33cc2a6e5207e984de0c2e693b8c00b8f8d35949d0bb7150484bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052431"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>Metodo CBaseReferenceClock.AdvisePeriodic

Il `AdvisePeriodic` metodo crea una richiesta di consulenza periodica. Questo metodo implementa il [**metodo IReferenceClock::AdvisePeriodic.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartTime* 
</dt> <dd>

Ora della prima notifica, in unità di 100 nanosecondi. Deve essere maggiore di zero e minore di MAX \_ TIME.

</dd> <dt>

*Periodo di tempo* 
</dt> <dd>

Tempo tra le notifiche, in unità di 100 nanosecondi. Deve essere maggiore di zero.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Handle per un semaforo, creato dal chiamante.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntatore a una variabile che riceve un identificatore per la richiesta di consulenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valori di ora non validi<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Operazioni non riuscite<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

A ogni ora di notifica, l'orologio rilascia il semaforo specificato nel *parametro hSemaphore.* Quando non sono necessarie altre notifiche, chiamare il metodo [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) e passare il valore *pdwAdviseToken* restituito da questa chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




