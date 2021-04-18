---
description: La funzione GetSubtypeName Recupera il nome leggibile di un sottotipo video.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Funzione GetSubtypeName (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330932"
---
# <a name="getsubtypename-function"></a>GetSubtypeName (funzione)

La `GetSubtypeName` funzione recupera il nome leggibile di un sottotipo video.

## <a name="syntax"></a>Sintassi


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSubtype* 
</dt> <dd>

Puntatore a un **GUID** del sottotipo video.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa contenente il nome.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




