---
description: Il metodo InitAllocator crea un allocatore di memoria.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: Metodo CBaseOutputPin.InitAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332059"
---
# <a name="cbaseoutputpininitallocator-method"></a>Metodo tAllocator CBaseOutputPin.Ini

Il `InitAllocator` metodo crea un allocatore di memoria.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAlloc* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un codice di errore della funzione **CoCreateInstance** .

## <a name="remarks"></a>Commenti

Se il pin di input non fornisce un allocatore di memoria, il metodo [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chiama questo metodo per creare un allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




