---
description: La funzione GetSubtypeName recupera il nome leggibile dell'utente di un sottotipo video.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Funzione GetSubtypeName (Wxutil.h)
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
ms.openlocfilehash: c676f3e08f55bd010e761853b777e0eb4b28933536ab7af09bd94e457032b583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564850"
---
# <a name="getsubtypename-function"></a>Funzione GetSubtypeName

La `GetSubtypeName` funzione recupera il nome leggibile dall'utente di un sottotipo video.

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

Puntatore a un sottotipo **video GUID**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa contenente il nome.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




