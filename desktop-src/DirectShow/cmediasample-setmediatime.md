---
description: 'Il metodo SetMediaTime imposta i tempi dei supporti per questo esempio. Questo metodo implementa il metodo IMediaSample:: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Metodo CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325308"
---
# <a name="cmediasamplesetmediatime-method"></a>CMediaSample. SetMediaTime, metodo

Il `SetMediaTime` metodo imposta i tempi dei supporti per questo esempio. Questo metodo implementa il metodo [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStart* 
</dt> <dd>

Puntatore all'ora di inizio del supporto o **null**.

</dd> <dt>

*Sospendere* 
</dt> <dd>

Puntatore all'ora di arresto del supporto o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

L'ora di arresto del supporto deve essere maggiore dell'ora di inizio del supporto. Usare **null** per invalidare i tempi dei supporti.

Il parametro *Pending* specifica un'ora assoluta dei supporti, ma la variabile membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) viene calcolata come offset da *PStart*. In altre parole, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

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

 

 




