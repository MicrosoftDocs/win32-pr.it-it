---
description: La funzione Int64x32Div32 implementa la formula ((a \* b) + Rnd)/c dove a è un valore a 64 bit e b, c e Rnd sono valori a 32 bit.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Funzione Int64x32Div32 (Wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332026"
---
# <a name="int64x32div32-function"></a>Int64x32Div32 (funzione)

La `Int64x32Div32` funzione implementa la formula `((a*b)+rnd)/c` in  cui è un valore a 64 bit e *b*, *c* e *Rnd* sono valori a 32 bit.

## <a name="syntax"></a>Sintassi


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
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

I timestamp e i tempi di ricerca sono valori a 64 bit, pertanto questa funzione è utile per l'esecuzione di conversioni su sistemi a 32 bit. Ad esempio, in MPEG-1 il riferimento all'orologio di sistema è 90-kHz o 90.000 tick al secondo. La formula per convertire questo oggetto in ora di riferimento (unità 100-nanosecondo) è


```C++
(timestamp * 1000) / 9
```



che può essere calcolato come `Int64x32Div32(timestamp, 1000, 9, 0)` . Usare il parametro *Rnd* come fattore di arrotondamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




