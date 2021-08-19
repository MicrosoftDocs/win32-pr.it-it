---
description: Il metodo GetSampleTimes recupera i timestamp da un esempio.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Metodo CBaseRenderer.GetSampleTimes (Renbase.h)
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
ms.openlocfilehash: 2d759cbcf2a9638b54e6194bcac7e7b24254c0d37987995d511fb4ffce85f1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954960"
---
# <a name="cbaserenderergetsampletimes-method"></a>Metodo CBaseRenderer.GetSampleTimes

Il `GetSampleTimes` metodo recupera i timestamp da un esempio.

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                                    | Descrizione                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                           | Il rendering dell'esempio deve essere eseguito immediatamente.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                        | L'esempio deve essere pianificato per il rendering, in base ai timestamp.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                         | Non eseguire il rendering di questo esempio.<br/>                                              |
| <dl> <dt>**VFW \_ E ORA DI INIZIO DOPO LA \_ \_ \_ \_ FINE**</dt> </dl> | Timestamp non erato: l'ora di fine è precedente all'ora di inizio.<br/>            |



 

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo per determinare come deve gestire un campione. Se il valore restituito è S \_ OK, il filtro esegue immediatamente il rendering dell'esempio. Se il valore restituito è S \_ FALSE, il filtro pianifica l'esempio per il rendering, in base ai timestamp. Se il valore restituito è un codice di errore, il filtro rifiuta l'esempio.

Questo metodo restituisce S OK se l'esempio non ha timestamp o se il filtro \_ non ha un orologio di riferimento. In caso contrario, restituisce il valore del [**metodo CBaseRenderer::ShouldDrawSampleNow.**](cbaserenderer-shoulddrawsamplenow.md) Nella classe di base **ShouldDrawSampleNow** restituisce sempre S \_ FALSE. La classe derivata può eseguire l'override di questo comportamento. Ad esempio, se la classe derivata implementa la gestione del controllo di qualità, potrebbe restituire E \_ FAIL per eliminare un campione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




