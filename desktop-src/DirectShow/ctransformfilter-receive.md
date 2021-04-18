---
description: Il metodo Receive riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Metodo CTransformFilter. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331129"
---
# <a name="ctransformfilterreceive-method"></a>Metodo CTransformFilter. Receive

Il `Receive` metodo riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream.

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

Il pin di input del filtro chiama questo metodo quando riceve un campione. Questo metodo chiama il metodo [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , che prepara un nuovo esempio di output. Chiama quindi il metodo [**CTransformFilter:: Transform**](ctransformfilter-transform.md) , che deve essere implementato dalla classe derivata. Il metodo **Transform** elabora i dati di input e produce i dati di output.

Se il metodo **Transform** restituisce \_ false, il `Receive` metodo elimina questo esempio. Nel primo esempio eliminato, il filtro Invia un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) al gestore del grafico dei filtri. In caso contrario, se il metodo **Transform** restituisce S \_ OK, il filtro recapita l'esempio di output. A tale scopo, viene chiamato il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




