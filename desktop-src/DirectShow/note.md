---
description: La macro nota Invia una stringa al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Nota (Wxdebug. h)
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
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332632"
---
# <a name="note"></a>NOTA

La `NOTE` macro invia una stringa al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.

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

Stringa di formato in stile printf.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*-*arg5*
</dt> <dd>

Argomenti aggiuntivi per la stringa di formato. Il numero di argomenti deve corrispondere al nome della macro. Ad esempio, **Note1** accetta un argomento e **NOTE5** accetta cinque argomenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

Queste macro sono varianti della macro [**DbgLog**](dbglog.md) . Generano messaggi di traccia del LOG di livello 5 \_ .

## <a name="example"></a>Esempio


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




