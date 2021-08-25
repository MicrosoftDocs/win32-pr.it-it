---
description: 'Metodo CTransformFilter.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer del pin di output.'
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Metodo CTransformFilter.DecideBufferSize (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1aba3ec43318079a73f0c94c8446b637ece29a5b61752462eeb8fc5898f5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907701"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>Metodo CTransformFilter.DecideBufferSize

Il `DecideBufferSize` metodo imposta i requisiti del buffer del pin di output.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) nell'allocatore del pin di output.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntatore a una [**struttura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer dal pin di input downstream.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Il metodo [**CTransformOutputPin::D ecideBufferSize**](ctransformoutputpin-decidebuffersize.md) del pin di output chiama questo metodo. La classe derivata deve implementare questo metodo. Per altre informazioni, vedere [**CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




