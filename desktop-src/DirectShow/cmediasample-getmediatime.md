---
description: Il metodo GetMediaTime recupera gli orari dei supporti per questo esempio. Questo metodo implementa il metodo IMediaSample::GetMediaTime.
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Metodo CMediaSample.GetMediaTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901531b3aaff882700a6a6196330cc7b0823b8b0069024101953f5f79a54e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634681"
---
# <a name="cmediasamplegetmediatime-method"></a>Metodo CMediaSample.GetMediaTime

Il `GetMediaTime` metodo recupera i tempi dei supporti per questo esempio. Questo metodo implementa il [**metodo IMediaSample::GetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di inizio del supporto.

</dd> <dt>

*Pend* 
</dt> <dd>

Puntatore a una variabile che riceve il tempo di arresto del supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ MEDIA \_ TIME \_ NOT \_ SET**</dt> </dl> | Per questo esempio non è stato impostato alcun tempo multimediale.<br/> |



 

## <a name="remarks"></a>Commenti

La variabile membro [**CMediaSample::m \_ MediaEnd**](cmediasample-m-mediaend.md) specifica un offset da [**CMediaSample::m \_ MediaStart**](cmediasample-m-mediastart.md), ma il valore ricevuto dal *parametro pEnd* è un tempo multimediale assoluto, calcolato come **m \_ MediaStart**  +  **m \_ MediaEnd**.

Per informazioni sugli orari dei supporti, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




