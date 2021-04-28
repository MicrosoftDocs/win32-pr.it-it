---
description: 'Metodo CBaseOutputPin.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer.'
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Metodo CBaseOutputPin.DecideBufferSize (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099529"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>Metodo CBaseOutputPin.DecideBufferSize

Il `DecideBufferSize` metodo imposta i requisiti del buffer.

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

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntatore a una [**struttura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer del pin di input. Se il pin di input non ha requisiti, il chiamante deve azzerare i membri di questa struttura prima di chiamare il metodo .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo nella classe derivata. Chiamare il [**metodo IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) per specificare i requisiti del buffer. In genere, la classe derivata rispetta i requisiti del buffer del pin di input, ma non è necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




