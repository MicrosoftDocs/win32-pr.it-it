---
description: La macro REMIND genera un promemoria in fase di compilazione. Questa macro genera una stringa che include la stringa del parametro, il nome del file di origine e il numero di riga.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: REMIND (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17ec8fac190cd98803a0dfa85acff015d0ac2c18ce712cc87316dd2dca181bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952120"
---
# <a name="remind"></a>Ricordare

La `REMIND` macro genera un promemoria in fase di compilazione. Questa macro genera una stringa che include la stringa del parametro, il nome del file di origine e il numero di riga.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Stringa di testo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa macro è utile per la generazione di avvisi in fase di compilazione:


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




