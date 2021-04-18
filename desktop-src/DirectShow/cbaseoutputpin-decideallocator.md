---
description: Il metodo DecideAllocator seleziona un allocatore di memoria.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Metodo CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329546"
---
# <a name="cbaseoutputpindecideallocator-method"></a>CBaseOutputPin. DecideAllocator, metodo

Il `DecideAllocator` metodo seleziona un allocatore di memoria.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del PIN di input.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato alla fine del processo di connessione del PIN. Esegue i passaggi seguenti:

1.  Chiama il metodo [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) per recuperare i requisiti del buffer del PIN di input, se presenti.
2.  Chiama il metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) per richiedere un allocatore dal pin di input. Se il pin di input non fornisce un allocatore, il pin di output ne crea uno chiamando il metodo della classe [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) .
3.  Chiama il metodo della classe [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , che imposta le proprietà dell'allocatore. Si tratta di un metodo virtuale puro. la classe derivata deve implementarla.
4.  Chiama il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , che invia una notifica al pin di input dell'allocatore usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




