---
description: La macro del nome genera una stringa di solo debug.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOME (Wxdebug. h)
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
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328074"
---
# <a name="name"></a>NAME

La macro del **nome** genera una stringa di solo debug.

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

Nelle build di debug questa macro è equivalente alla macro di **testo** . Nelle compilazioni finali, viene risolto in (TCHAR \* ) **null**. Questa macro è utile quando si dichiara il nome di un oggetto che deriva dalla classe [**CBaseObject**](cbaseobject.md) .


```C++
pObject = new CBaseObject(NAME("My Object"));
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

 

 




