---
description: 'Il metodo run esegue il filtro. Questo metodo implementa il metodo IMediaFilter:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Metodo CBaseFilter. Run (Amfilter. h)
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
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326941"
---
# <a name="cbasefilterrun-method"></a>Metodo CBaseFilter. Run

Il `Run` metodo esegue il filtro. Questo metodo implementa il metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

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

Tempo di riferimento corrispondente all'ora del flusso 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="remarks"></a>Commenti

Se il filtro viene arrestato, questo metodo sospende il filtro chiamando il metodo [**CBaseFilter::P ause**](cbasefilter-pause.md) . Chiama quindi il metodo [**CBasePin:: Run**](cbasepin-run.md) su ognuno dei pin connessi del filtro. Infine, imposta la variabile membro di [**\_ stato CBaseFilter:: m**](cbasefilter-m-state.md) sullo stato \_ in esecuzione.

Il tempo di flusso viene calcolato come ora di riferimento corrente meno *tStart*. È necessario eseguire il rendering di un campione multimediale con un timestamp di zero all'ora *tStart*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




