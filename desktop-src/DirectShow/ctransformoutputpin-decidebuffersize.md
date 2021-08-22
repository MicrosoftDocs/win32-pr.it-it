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
ms.openlocfilehash: 3c6ea09c348fa465e1bffac2bdf426b635ed4cb4b76013a053ab775e78199612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538221"
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
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




