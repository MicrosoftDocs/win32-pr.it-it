---
description: 'Il metodo AdvisePeriodic crea una richiesta di notifica periodica. Questo metodo implementa il metodo IReferenceClock:: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Metodo CBaseReferenceClock. AdvisePeriodic (Refclock. h)
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
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330305"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>CBaseReferenceClock. AdvisePeriodic, metodo

Il `AdvisePeriodic` metodo crea una richiesta di notifica periodica. Questo metodo implementa il metodo [**IReferenceClock:: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .

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

Ora della prima notifica, in unità di 100 nanosecondi. Deve essere maggiore di zero e minore del \_ tempo massimo.

</dd> <dt>

*PeriodTime* 
</dt> <dd>

Tempo tra le notifiche, in unità di 100 nanosecondi. Deve essere maggiore di zero.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Handle per un semaforo, creato dal chiamante.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntatore a una variabile che riceve un identificatore per la richiesta di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valori di ora non validi<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Errore<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

A ogni ora di notifica, il clock rilascia il semaforo specificato nel parametro *hSemaphore* . Quando non sono necessarie altre notifiche, chiamare il metodo [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) e passare il valore *pdwAdviseToken* restituito dalla chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




