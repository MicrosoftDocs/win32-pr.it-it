---
description: Il metodo GetSize recupera le dimensioni del buffer. Questo metodo implementa il metodo IMediaSample::GetSize.
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: Metodo CMediaSample.GetSize (Amfilter.h)
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
ms.openlocfilehash: f3559f972f35a01738c60f32414ab0b42a079032ac5bc6b3ab0e5b7212900d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156752"
---
# <a name="cmediasamplegetsize-method"></a>Metodo CMediaSample.GetSize

Il `GetSize` metodo recupera le dimensioni del buffer. Questo metodo implementa il [**metodo IMediaSample::GetSize.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)

## <a name="syntax"></a>Sintassi


```C++
LONG GetSize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce le dimensioni del buffer, in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




