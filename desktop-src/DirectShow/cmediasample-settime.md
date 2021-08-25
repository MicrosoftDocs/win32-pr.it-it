---
description: Il metodo SetTime imposta le ore del flusso in cui questo esempio deve iniziare e terminare. Questo metodo implementa il metodo IMediaSample::SetTime.
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Metodo CMediaSample.SetTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be9028db35cb6d74623bde77fac21e32793de436ea2f80d2f513687c15d1b64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156513"
---
# <a name="cmediasamplesettime-method"></a>Metodo CMediaSample.SetTime

Il `SetTime` metodo imposta i tempi del flusso quando questo esempio deve iniziare e terminare. Questo metodo implementa il [**metodo IMediaSample::SetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Puntatore all'ora del flusso in cui inizia il campione, in unità di 100 nanosecondi, o **NULL.**

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntatore all'ora del flusso in cui termina il campione, in unità di 100 nanosecondi, **o NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta le variabili membro Start e [**CMediaSample::m \_ End di CMediaSample::m,**](cmediasample-m-end.md) che specificano i timestamp. [**\_**](cmediasample-m-start.md) Aggiorna anche la variabile membro [**\_ dwFlags CMediaSample::m,**](cmediasample-m-dwflags.md) che specifica se i timestamp sono validi.

Per informazioni sui timestamp, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




