---
description: 'Metodo CBaseOutputPin.CompleteConnect: il metodo CompleteConnect completa una connessione a un pin di input.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Metodo CBaseOutputPin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099539"
---
# <a name="cbaseoutputpincompleteconnect-method"></a>Metodo CBaseOutputPin.CompleteConnect

Il `CompleteConnect` metodo completa una connessione a un pin di input.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore al pin di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::CompleteConnect.**](cbasepin-completeconnect.md) Chiama il [**metodo DecideAllocator,**](cbaseoutputpin-decideallocator.md) che seleziona l'allocatore di memoria da usare per questa connessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




