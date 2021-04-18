---
description: "Il metodo run esegue l'oggetto. Questo metodo implementa il metodo IMediaFilter:: Run."
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Metodo CBaseMediaFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325075"
---
# <a name="cbasemediafilterrun-method"></a>Metodo CBaseMediaFilter. Run

Il `Run` metodo esegue l'oggetto. Questo metodo implementa il metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

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

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Se l'oggetto viene arrestato, questo metodo sospende l'oggetto chiamando il metodo [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md) . Imposta quindi la variabile membro di [**\_ stato CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) sullo stato \_ in esecuzione.

Il tempo di flusso viene calcolato come ora di riferimento corrente meno *tStart*. È necessario eseguire il rendering di un campione multimediale con un timestamp di zero all'ora *tStart*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




