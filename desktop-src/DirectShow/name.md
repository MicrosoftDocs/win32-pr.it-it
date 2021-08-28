---
description: La macro NAME genera una stringa di solo debug.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NAME (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107681"
---
# <a name="name"></a>NOME

La macro **NAME** genera una stringa di solo debug.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Stringa di testo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nelle build di debug questa macro è equivalente alla macro **TEXT.** Nelle build per la vendita al dettaglio viene risolto in (TCHAR \* ) **NULL.** Questa macro è utile quando si dichiara il nome di un oggetto che deriva dalla [**classe CBaseObject.**](cbaseobject.md)


```C++
pObject = new CBaseObject(NAME("My Object"));
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

 

 




