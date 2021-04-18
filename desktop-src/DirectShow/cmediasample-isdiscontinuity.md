---
description: "Il metodo IsDiscontinuity determina se l'esempio rappresenta un'operazione break nel flusso di dati. Questo metodo implementa il metodo IMediaSample:: IsDiscontinuity."
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Metodo CMediaSample. IsDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324957"
---
# <a name="cmediasampleisdiscontinuity-method"></a>CMediaSample. IsDiscontinuity, metodo

Il `IsDiscontinuity` metodo determina se l'esempio rappresenta un'interruzioni nel flusso di dati. Questo metodo implementa il metodo [**IMediaSample:: IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esempio è un'interruzioni nel flusso di dati e in \_ caso contrario è false.

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

 

 




