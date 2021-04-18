---
description: 'Il metodo GetSize recupera le dimensioni del buffer. Questo metodo implementa il metodo IMediaSample:: GetSize.'
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: Metodo CMediaSample. GetSize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324962"
---
# <a name="cmediasamplegetsize-method"></a>Metodo CMediaSample. GetSize

Il `GetSize` metodo recupera le dimensioni del buffer. Questo metodo implementa il metodo [**IMediaSample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) .

## <a name="syntax"></a>Sintassi


```C++
LONG GetSize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la dimensione, in byte, del buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




