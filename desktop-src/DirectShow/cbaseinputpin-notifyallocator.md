---
description: 'Il metodo NotifyAllocator specifica un allocatore per la connessione. Questo metodo implementa il metodo IMemInputPin:: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Metodo CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330701"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>CBaseInputPin. NotifyAllocator, metodo

Il `NotifyAllocator` metodo specifica un allocatore per la connessione. Questo metodo implementa il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Flag che specifica se gli esempi di questo allocatore sono di sola lettura. Se **true**, gli esempi sono di sola lettura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Durante la connessione del PIN, il pin di output sceglie un allocatore e chiama questo metodo per inviare una notifica al pin di input. Il pin di output può usare l'allocatore proposto dal pin di input nel metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) oppure può fornire il proprio allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




