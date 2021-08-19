---
description: La funzione Int64x32Div32 implementa la formula ((a \* b)+rnd)/c dove a è un valore a 64 bit e b, c e rnd sono valori a 32 bit.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Funzione Int64x32Div32 (Wxutil.h)
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
ms.openlocfilehash: a56425d1f07346f8e546940ff5880416e4e63efc692974c78f0e344b9ec01c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051591"
---
# <a name="int64x32div32-function"></a>Funzione Int64x32Div32

La funzione implementa la formula in cui a è un valore `Int64x32Div32` `((a*b)+rnd)/c` a 64 bit e *b*,  *c* e *rnd* sono valori a 32 bit.

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

*Un* 
</dt> <dd>

Moltiplicazione.

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

I timestamp e gli orari di ricerca sono valori a 64 bit, quindi questa funzione è utile per eseguire conversioni in sistemi a 32 bit. Ad esempio, in MPEG-1 il riferimento all'orologio di sistema è 90 kHz o 90.000 tick al secondo. La formula per convertirlo in ora di riferimento (unità di 100 nanosecondi) è


```C++
(timestamp * 1000) / 9
```



che può essere calcolato come `Int64x32Div32(timestamp, 1000, 9, 0)` . Usare il *parametro rnd* come fattore di arrotondamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




