---
description: Il metodo Run esegue il filtro. Questo metodo implementa il metodo IMediaFilter::Run.
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Metodo CBaseFilter.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793281"
---
# <a name="cbasefilterrun-method"></a>Metodo CBaseFilter.Run

Il `Run` metodo esegue il filtro. Questo metodo implementa il [**metodo IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Ora di riferimento corrispondente all'ora del flusso 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Se il filtro viene arrestato, questo metodo sospende il filtro chiamando il metodo [**CBaseFilter::P ause.**](cbasefilter-pause.md) Chiama quindi il [**metodo CBasePin::Run**](cbasepin-run.md) su ognuno dei pin connessi del filtro. Infine, imposta la variabile membro [**CBaseFilter::m \_ State**](cbasefilter-m-state.md) su State \_ Running.

L'ora del flusso viene calcolata come ora di riferimento corrente meno *tStart*. Il rendering di un campione multimediale con timestamp pari a zero deve essere eseguito al momento *tStart*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




