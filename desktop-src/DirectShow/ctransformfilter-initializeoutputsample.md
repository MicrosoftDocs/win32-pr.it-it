---
description: Il metodo InitializeOutputSample recupera un nuovo esempio di output e lo inizializza.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Inimetodo tializeOutputSample (Transfrm.h)
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
ms.openlocfilehash: 083867f2ef6b2e40462112036dbbb000c25bc3ad2bb443f011235e36bf245ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953620"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>CTransformFilter.Inimetodo tializeOutputSample

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

Puntatore all'interfaccia [**IMediaSample dell'esempio di**](/windows/desktop/api/Strmif/nn-strmif-imediasample) input.

</dd> <dt>

*ppOutSample* 
</dt> <dd>

Riceve un puntatore all'interfaccia **IMediaSample dell'esempio di** output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal metodo [**CTransformFilter::Receive**](ctransformfilter-receive.md) per preparare l'esempio di output. In genere non è necessario chiamare questo metodo nella classe derivata, a meno che non venga eseguito l'override **del metodo Receive.**

Questo metodo recupera un nuovo esempio dall'allocatore del pin di output. Copia quindi le proprietà di esempio dall'esempio di input all'esempio di output. Le proprietà di esempio sono definite nella [**struttura \_ AM SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




