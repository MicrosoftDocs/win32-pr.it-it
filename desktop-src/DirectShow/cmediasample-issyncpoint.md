---
description: Il metodo IsSyncPoint determina se l'inizio dell'esempio è un punto di sincronizzazione. Questo metodo implementa il metodo IMediaSample::IsSyncPoint.
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Metodo CMediaSample.IsSyncPoint (Amfilter.h)
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
ms.openlocfilehash: 00d238bb9289ba71237bfdf8e72acde384430f72470f16211093cb2ece8d68f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074005"
---
# <a name="cmediasampleissyncpoint-method"></a>Metodo CMediaSample.IsSyncPoint

Il `IsSyncPoint` metodo determina se l'inizio dell'esempio è un punto di sincronizzazione. Questo metodo implementa il [**metodo IMediaSample::IsSyncPoint.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se l'esempio è un punto di sincronizzazione oppure S \_ FALSE in caso contrario.

## <a name="remarks"></a>Commenti

La [**variabile membro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) specifica questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




