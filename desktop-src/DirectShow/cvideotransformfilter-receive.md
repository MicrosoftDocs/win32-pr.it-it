---
description: Il metodo Receive riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream. Questo metodo esegue l'override del metodo CTransformFilter::Receive.
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Metodo CVideoTransformFilter.Receive (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bce69d5f14a522f403eed54b56a340ab02316507766c0cc6d60ff897ec73541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998511"
---
# <a name="cvideotransformfilterreceive-method"></a>Metodo CVideoTransformFilter.Receive

Il `Receive` metodo riceve un campione multimediale, lo elabora e fornisce un esempio di output al filtro downstream. Questo metodo esegue l'override [**del metodo CTransformFilter::Receive.**](ctransformfilter-receive.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) nell'esempio di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                             | Descrizione                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il filtro upstream deve interrompere l'invio di campioni.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                         |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) per determinare se deve recapitare questo esempio o semplicemente eliminarlo. Se **ShouldSkipFrame** restituisce **FALSE** (che indica che l'esempio deve essere recapitato), il metodo esegue le operazioni seguenti:

1.  Chiama [**CTransformFilter::InitializeOutputSample per**](ctransformfilter-initializeoutputsample.md) preparare l'esempio di output
2.  Chiama [**CTransformFilter::Transform per**](ctransformfilter-transform.md) elaborare l'esempio di input. Questo metodo è virtuale puro e deve essere implementato nella classe derivata.
3.  Chiama [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) per fornire l'esempio di output.

Questo metodo verifica inoltre la presenza di modifiche di formato nell'esempio di input o output chiamando [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). In caso di modifica del formato, il metodo imposta il tipo di connessione sul pin corrispondente. Prima di impostare il nuovo tipo, chiama **StopStreaming.** Dopo aver impostato il nuovo tipo, chiama **StartStreaming.** La classe derivata può usare questi metodi per aggiornarne lo stato interno. La classe derivata potrebbe anche dover verificare la presenza del nuovo formato nel **relativo metodo Transform.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




