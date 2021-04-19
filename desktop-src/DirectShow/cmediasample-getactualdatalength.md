---
description: 'Il metodo GetActualDataLength recupera la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo IMediaSample:: GetActualDataLength.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Metodo CMediaSample. GetActualDataLength (Amfilter. h)
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
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332327"
---
# <a name="cmediasamplegetactualdatalength-method"></a>CMediaSample. GetActualDataLength, metodo

Il `GetActualDataLength` metodo recupera la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .

## <a name="syntax"></a>Sintassi


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza in byte dei dati validi.

## <a name="remarks"></a>Commenti

La variabile membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) specifica questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

