---
description: La funzione llMulDiv implementa la formula ((a \* b)+rnd)/c in cui ogni termine è un valore a 64 bit.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: Funzione llMulDiv (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df58175955106906027a6d2d10c465b82ad6313cd493e3ef9ef3ba279cd0115f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952350"
---
# <a name="llmuldiv-function"></a>Funzione llMulDiv

La `llMulDiv` funzione implementa la formula in cui ogni termine è un valore a `((a*b)+rnd)/c` 64 bit.

I timestamp e gli orari di ricerca sono valori a 64 bit, quindi questa funzione è utile per eseguire conversioni in sistemi a 32 bit. Ad esempio, la formula per byte al secondo è


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



che può essere calcolato come `llMulDiv(nBytes, rtTime, 10000000, 0)` . Usare il *parametro rnd* come fattore di arrotondamento.

## <a name="syntax"></a>Sintassi


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Un* 
</dt> <dd>

Moltiplicato.

</dd> <dt>

*b* 
</dt> <dd>

Moltiplicatore.

</dd> <dt>

*c* 
</dt> <dd>

Divisore.

</dd> <dt>

*Rnd* 
</dt> <dd>

Fattore di arrotondamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il `(a * b + rnd)/c` calcolo o uno dei valori seguenti.



| Codice restituito                                                                                       | Descrizione                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Si è verificato un overflow perché il risultato è troppo grande (positivo).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Si è verificato un overflow perché il risultato è troppo grande (negativo).<br/> |



 

## <a name="remarks"></a>Commenti

L'arrotondamento sulla divisione è verso zero. La divisione per zero viene conteggiata come condizione di overflow.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




