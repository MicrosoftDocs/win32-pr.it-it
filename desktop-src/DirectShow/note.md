---
description: La macro NOTE invia una stringa al percorso di output di debug. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: NOTA (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0becacba37f3f474577c36a694539de77795f1c19ccf3b1655cb80370be9e297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050921"
---
# <a name="note"></a>NOTA

La `NOTE` macro invia una stringa al percorso di output di debug. Ignorato nelle build per la vendita al dettaglio.

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*
</dt> <dd>

Stringa di formato di tipo printf.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*
</dt> <dd>

Argomenti aggiuntivi per la stringa di formato. Il numero di argomenti deve corrispondere al nome della macro. Ad esempio, **NOTE1** accetta un argomento e **NOTE5** accetta cinque argomenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

Queste macro sono varianti della macro [**DbgLog.**](dbglog.md) Generano messaggi LOG \_ TRACE di livello 5.

## <a name="example"></a>Esempio


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
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

 

 




