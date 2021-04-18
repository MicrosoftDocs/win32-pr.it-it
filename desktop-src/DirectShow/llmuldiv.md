---
description: La funzione llMulDiv implementa la formula ((a \* b) + Rnd)/c, dove ogni termine è un valore a 64 bit.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: funzione llMulDiv (Wxutil. h)
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
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327421"
---
# <a name="llmuldiv-function"></a>llMulDiv (funzione)

La `llMulDiv` funzione implementa la formula in `((a*b)+rnd)/c` cui ogni termine è un valore a 64 bit.

I timestamp e i tempi di ricerca sono valori a 64 bit, pertanto questa funzione è utile per l'esecuzione di conversioni su sistemi a 32 bit. Ad esempio, la formula per byte al secondo è


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



che può essere calcolato come `llMulDiv(nBytes, rtTime, 10000000, 0)` . Usare il parametro *Rnd* come fattore di arrotondamento.

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

*un* 
</dt> <dd>

Multiplicand.

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

L'arrotondamento alla divisione è verso lo zero. La divisione per zero viene conteggiata come condizione di overflow.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




