---
description: "Metodo CBaseFilter.StreamTime: il metodo StreamTime recupera l'ora corrente del flusso."
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Metodo CBaseFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120069"
---
# <a name="cbasefilterstreamtime-method"></a>Metodo CBaseFilter.StreamTime

Il **metodo StreamTime** recupera l'ora corrente del flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Riferimento a un [**oggetto CRefTime**](creftime.md) che riceve l'ora corrente del flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                      | Descrizione                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Operazione completata.<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | Non è disponibile alcun orologio di riferimento.<br/> |



 

## <a name="remarks"></a>Commenti

L'ora di flusso è definita come ora di riferimento corrente (come specificato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseFilter::m \_ tStart**](cbasefilter-m-tstart.md)). Il timestamp di un campione *multimediale* specifica l'ora del flusso in cui deve essere eseguito il rendering. Se non è ancora stato eseguito il rendering di un esempio con timestamp inferiore all'ora corrente del flusso, è in ritardo.

Questo metodo ottiene l'ora del flusso chiamando [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente e quindi sottraendo l'ora di inizio iniziale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




