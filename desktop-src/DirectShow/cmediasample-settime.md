---
description: 'Il metodo setime imposta il flusso di tempo quando questo esempio deve iniziare e terminare. Questo metodo implementa il metodo IMediaSample:: setime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Metodo CMediaSample. setime (Amfilter. h)
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
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324024"
---
# <a name="cmediasamplesettime-method"></a>CMediaSample. setime (metodo)

Il `SetTime` metodo imposta il flusso di tempo quando questo esempio deve iniziare e terminare. Questo metodo implementa il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

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

Puntatore all'ora del flusso in cui inizia l'esempio, in unità di 100 nanosecondi o **null**.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntatore all'ora del flusso in cui termina il campione, in unità di 100 nanosecondi o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo imposta le variabili membro End [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample \_ :: m**](cmediasample-m-end.md) , che specificano i timestamp. Viene inoltre aggiornata la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica se i timestamp sono validi.

Per informazioni sui timestamp, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




