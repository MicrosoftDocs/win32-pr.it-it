---
description: Il metodo DecideAllocator seleziona un allocatore di memoria.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Metodo CBaseOutputPin.DecideAllocator (Amfilter.h)
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
ms.openlocfilehash: 73d822450d635fe5f7620d59f39fcc7ed85fe1e2465f34af3ef561dfc2f3828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814211"
---
# <a name="cbaseoutputpindecideallocator-method"></a>Metodo CBaseOutputPin.DecideAllocator

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

Puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del pin di input.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato alla fine del processo di connessione pin. Esegue i passaggi seguenti:

1.  Chiama il [**metodo IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) per recuperare i requisiti del buffer del pin di input, se presenti.
2.  Chiama il [**metodo IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) per richiedere un allocatore dal pin di input. Se il pin di input non fornisce un allocatore, il pin di output ne crea uno chiamando il metodo della classe [**CBaseOutputPin::InitAllocator.**](cbaseoutputpin-initallocator.md)
3.  Chiama il [**metodo della classe CBaseOutputPin::D ecideBufferSize,**](cbaseoutputpin-decidebuffersize.md) che imposta le proprietà dell'allocatore. Si tratta di un metodo virtuale puro. la classe derivata deve implementarla.
4.  Chiama il [**metodo IMemInputPin::NotifyAllocator,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) che notifica al pin di input l'allocatore in uso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




