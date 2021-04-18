---
description: "Il metodo Receive riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream. Questo metodo esegue l'override del metodo CTransformFilter:: Receive."
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Metodo CVideoTransformFilter. Receive (Vtrans. h)
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
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328628"
---
# <a name="cvideotransformfilterreceive-method"></a>Metodo CVideoTransformFilter. Receive

Il `Receive` metodo riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream. Questo metodo esegue l'override del metodo [**CTransformFilter:: Receive**](ctransformfilter-receive.md) .

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

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) nell'esempio di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                             | Descrizione                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il filtro upstream deve interrompere l'invio degli esempi.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                         |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama [**CVideoTransformFilter:: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) per determinare se deve fornire questo esempio o semplicemente rimuoverlo. Se **ShouldSkipFrame** restituisce **false** (che indica che l'esempio deve essere recapitato), il metodo esegue le operazioni seguenti:

1.  Chiama [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) per preparare l'esempio di output
2.  Chiama [**CTransformFilter:: Transform**](ctransformfilter-transform.md) per elaborare l'esempio di input. Questo metodo è virtuale puro e deve essere implementato nella classe derivata.
3.  Chiama [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) per recapitare l'esempio di output.

Questo metodo, inoltre, verifica le modifiche di formato nell'esempio di input o di output, chiamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Se viene apportata una modifica al formato, il metodo imposta il tipo di connessione sul pin corrispondente. Prima di impostare il nuovo tipo, viene chiamato **StopStreaming**. Dopo aver impostato il nuovo tipo, viene chiamato **StartStreaming**. La classe derivata può usare questi metodi per aggiornarne lo stato interno. La classe derivata potrebbe anche dover verificare il nuovo formato nel metodo **Transform** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




