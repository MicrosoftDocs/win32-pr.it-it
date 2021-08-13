---
description: Il metodo GetTime recupera l'ora del flusso in cui questo esempio deve iniziare e terminare. Questo metodo implementa il metodo IMediaSample::GetTime.
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Metodo CMediaSample.GetTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 755965864692cf2b34ebaadc6e064a47a7514c69fe891a6a15f1bb364e5345e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655252"
---
# <a name="cmediasamplegettime-method"></a>Metodo CMediaSample.GetTime

Il metodo recupera l'ora di inizio e fine del flusso in `GetTime` cui questo esempio deve iniziare e terminare. Questo metodo implementa il [**metodo IMediaSample::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora del flusso iniziale, in unità da 100 nanosecondi.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora del flusso finale, in unità da 100 nanosecondi. Se l'esempio non ha ora di arresto, il valore viene impostato sull'ora di inizio più uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                   | Descrizione                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Operazione completata.<br/>                                         |
| <dl> <dt>**VFW \_ S \_ NO \_ STOP \_ TIME**</dt> </dl>         | L'esempio ha un'ora di inizio valida, ma non un'ora di arresto.<br/> |
| <dl> <dt>**ORA DI ESEMPIO VFW \_ E \_ NON \_ \_ \_ IMPOSTATA**</dt> </dl> | L'esempio non ha timestamp validi.<br/>          |



 

## <a name="remarks"></a>Commenti

Le [**variabili membro CMediaSample::m \_ Start**](cmediasample-m-start.md) e [**CMediaSample::m \_ End**](cmediasample-m-end.md) specificano i timestamp. La variabile membro [**CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) specifica se i timestamp sono validi.

Per informazioni sui timestamp, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




