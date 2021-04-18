---
description: La funzione GetBitCount restituisce il numero di bit per pixel usato da un sottotipo video specificato. Questa funzione è valida solo per sottotipi RGB non compressi.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Funzione GetBitCount (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328251"
---
# <a name="getbitcount-function"></a>GetBitCount (funzione)

La `GetBitCount` funzione restituisce il numero di bit per pixel utilizzato da un sottotipo video specificato. Questa funzione è valida solo per sottotipi RGB non compressi.

## <a name="syntax"></a>Sintassi


```C++
WORD GetBitCount(
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

Restituisce il numero di bit per pixel per questo sottotipo oppure il valore **USHRT \_ Max** se il sottotipo non è riconosciuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




