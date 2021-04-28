---
description: 'Metodo CTransformOutputPin.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Metodo CTransformOutputPin.DecideBufferSize (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084839"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>Metodo CTransformOutputPin.DecideBufferSize

Il `DecideBufferSize` metodo imposta i requisiti del buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntatore a [**una struttura \_ ALLOCATOR PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer del pin di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseOutputPin::D ecideBufferSize.**](cbaseoutputpin-decidebuffersize.md) Chiama il metodo [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) virtuale puro del filtro, che deve essere implementato dalla classe derivata del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




