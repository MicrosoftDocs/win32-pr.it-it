---
description: Il metodo GetActualDataLength recupera la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo IMediaSample::GetActualDataLength.
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Metodo CMediaSample.GetActualDataLength (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d41c23e45ba65416a0f57336e51d2784b194ee556a778b7036e8dc5fd829ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016389"
---
# <a name="cmediasamplegetactualdatalength-method"></a>Metodo CMediaSample.GetActualDataLength

Il `GetActualDataLength` metodo recupera la lunghezza dei dati validi nel buffer. Questo metodo implementa il [**metodo IMediaSample::GetActualDataLength.**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength)

## <a name="syntax"></a>Sintassi


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza dei dati validi, in byte.

## <a name="remarks"></a>Commenti

La [**variabile membro CMediaSample::m \_ lActual**](cmediasample-m-lactual.md) specifica questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

