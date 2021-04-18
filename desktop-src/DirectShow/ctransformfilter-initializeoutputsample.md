---
description: Il metodo InitializeOutputSample recupera un nuovo esempio di output e lo inizializza.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: Metodo CTransformFilter.InitializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331149"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>Metodo tializeOutputSample CTransformFilter.Ini

Il `InitializeOutputSample` metodo recupera un nuovo esempio di output e lo inizializza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio di input.

</dd> <dt>

*ppOutSample* 
</dt> <dd>

Riceve un puntatore all'interfaccia **IMediaSample** dell'esempio di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal metodo [**CTransformFilter:: Receive**](ctransformfilter-receive.md) per preparare l'esempio di output. In genere non è necessario chiamare questo metodo nella classe derivata, a meno che non si esegua l'override del metodo **Receive** .

Questo metodo recupera un nuovo campione dall'allocatore del PIN di output. Quindi copia le proprietà di esempio dall'esempio di input nell'esempio di output. Le proprietà di esempio sono definite nella struttura delle [**\_ \_ Proprietà am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




