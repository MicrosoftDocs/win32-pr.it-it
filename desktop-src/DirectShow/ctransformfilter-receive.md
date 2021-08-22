---
description: Il metodo Receive riceve un campione di supporti, lo elabora e recapita un esempio di output al filtro downstream.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Metodo CTransformFilter.Receive (Transfrm.h)
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
ms.openlocfilehash: 6a0c57cf6826274169a5984dd794e1ba9a5b8e78c7ffb774b00b05f16384e4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953410"
---
# <a name="ctransformfilterreceive-method"></a>Metodo CTransformFilter.Receive

Il `Receive` metodo riceve un campione di supporti, lo elabora e recapita un esempio di output al filtro downstream.

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

Il pin di input del filtro chiama questo metodo quando riceve un esempio. Questo metodo chiama il [**metodo CTransformFilter::InitializeOutputSample,**](ctransformfilter-initializeoutputsample.md) che prepara un nuovo esempio di output. Chiama quindi il [**metodo CTransformFilter::Transform,**](ctransformfilter-transform.md) che deve essere implementato dalla classe derivata. Il **metodo Transform** elabora i dati di input e produce dati di output.

Se il **metodo Transform** restituisce S \_ FALSE, il metodo elimina questo `Receive` esempio. Nel primo esempio eliminato, il filtro invia un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al gestore del grafico dei filtri. In caso contrario, se **il metodo Transform** restituisce S \_ OK, il filtro restituisce l'esempio di output. A tale scopo, chiama il [**metodo IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




