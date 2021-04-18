---
description: "Il metodo getTime recupera le ore del flusso in cui l'esempio deve iniziare e terminare. Questo metodo implementa il metodo IMediaSample:: GetTime."
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Metodo CMediaSample. getTime (Amfilter. h)
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
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324958"
---
# <a name="cmediasamplegettime-method"></a>CMediaSample. getTime, metodo

Il `GetTime` metodo recupera l'ora del flusso in cui l'esempio deve iniziare e terminare. Questo metodo implementa il metodo [**IMediaSample:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .

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

Puntatore a una variabile che riceve l'ora di inizio del flusso, in unità di 100 nanosecondi.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora del flusso finale, in unità di 100 nanosecondi. Se l'esempio non ha tempo di arresto, il valore viene impostato sull'ora di inizio più uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                   | Descrizione                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                          | Esito positivo.<br/>                                         |
| <dl> <dt>**\_ \_ nessun tempo di \_ arresto \_ per il VFW**</dt> </dl>         | L'esempio ha un'ora di inizio valida, ma nessuna ora di arresto.<br/> |
| <dl> <dt>**tempo di esempio di VFW \_ E \_ \_ \_ non \_ impostato**</dt> </dl> | L'esempio non dispone di timestamp validi.<br/>          |



 

## <a name="remarks"></a>Commenti

Le variabili membro End [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample \_ :: m**](cmediasample-m-end.md) specificano i timestamp. La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica se i timestamp sono validi.

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

 

 




