---
description: La funzione EqualPins controlla se due pin si trovano nello stesso oggetto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Funzione EqualPins (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325181"
---
# <a name="equalpins-function"></a>EqualPins (funzione)

La funzione EqualPins controlla se due pin si trovano nello stesso oggetto.

## <a name="syntax"></a>Sintassi


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin1* 
</dt> <dd>

Puntatore a un PIN.

</dd> <dt>

*pPin2* 
</dt> <dd>

Puntatore all'altro pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se entrambi i pin si trovano nello stesso oggetto. in caso contrario, **false** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




