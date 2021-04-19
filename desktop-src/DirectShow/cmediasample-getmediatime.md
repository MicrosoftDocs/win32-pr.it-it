---
description: 'Il metodo GetMediaTime recupera i tempi dei supporti per questo esempio. Questo metodo implementa il metodo IMediaSample:: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Metodo CMediaSample. GetMediaTime (Amfilter. h)
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
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326406"
---
# <a name="cmediasamplegetmediatime-method"></a>CMediaSample. GetMediaTime, metodo

Il `GetMediaTime` metodo recupera i tempi di supporto per questo esempio. Questo metodo implementa il metodo [**IMediaSample:: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStart* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di inizio del supporto.

</dd> <dt>

*Sospendere* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di arresto del supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                                 |
| <dl> <dt>**\_ \_ tempo medio E \_ \_ non \_ impostato per VFW**</dt> </dl> | Non sono stati impostati tempi multimediali per questo esempio.<br/> |



 

## <a name="remarks"></a>Commenti

La variabile membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) specifica un offset da [**CMediaSample:: m \_ MediaStart**](cmediasample-m-mediastart.md), ma il valore ricevuto dal parametro *Pending* è un tempo di supporto assoluto, calcolato come **m \_ MediaStart**  +  **m \_ MediaEnd**.

Per informazioni sui tempi dei supporti, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




