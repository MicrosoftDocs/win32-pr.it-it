---
description: Il metodo GetSampleTimes recupera i timestamp da un campione.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Metodo CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325933"
---
# <a name="cbaserenderergetsampletimes-method"></a>CBaseRenderer. GetSampleTimes, metodo

Il `GetSampleTimes` metodo recupera i timestamp da un campione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di inizio.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di fine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                    | Descrizione                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                           | Il rendering dell'esempio deve essere eseguito immediatamente.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>                        | L'esempio deve essere pianificato per il rendering, in base agli indicatori temporali.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                         | Non eseguire il rendering di questo esempio.<br/>                                              |
| <dl> <dt>**ora di inizio di VFW \_ E \_ dopo la \_ \_ \_ fine**</dt> </dl> | Timestamp non valido: l'ora di fine è precedente all'ora di inizio.<br/>            |



 

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo per determinare la modalità di gestione di un campione. Se il valore restituito è S \_ OK, il filtro esegue immediatamente il rendering dell'esempio. Se il valore restituito è S \_ false, il filtro pianifica l'esempio per il rendering in base ai timestamp. Se il valore restituito è un codice di errore, il filtro rifiuterà l'esempio.

Questo metodo restituisce \_ OK se l'esempio non dispone di timestamp o se il filtro non dispone di un clock di riferimento. In caso contrario, restituisce il valore del metodo [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) . Nella classe di base, **ShouldDrawSampleNow** restituisce sempre \_ false. La classe derivata può eseguire l'override di questo comportamento. Se, ad esempio, la classe derivata implementa la gestione del controllo di qualità, potrebbe restituire E \_ non riuscire a eliminare un campione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




