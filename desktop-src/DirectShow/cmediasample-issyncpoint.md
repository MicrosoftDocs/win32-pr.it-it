---
description: "Il metodo IsSyncPoint determina se l'inizio dell'esempio è un punto di sincronizzazione. Questo metodo implementa il metodo IMediaSample:: IsSyncPoint."
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Metodo CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324952"
---
# <a name="cmediasampleissyncpoint-method"></a>CMediaSample. IsSyncPoint, metodo

Il `IsSyncPoint` metodo determina se l'inizio dell'esempio è un punto di sincronizzazione. Questo metodo implementa il metodo [**IMediaSample:: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esempio è un punto di sincronizzazione, oppure S \_ false in caso contrario.

## <a name="remarks"></a>Commenti

La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




