---
description: Il metodo SetMediaTime imposta gli orari dei supporti per questo esempio. Questo metodo implementa il metodo IMediaSample::SetMediaTime.
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Metodo CMediaSample.SetMediaTime (Amfilter.h)
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
ms.openlocfilehash: 3709a5f487855148b8ad4042f61b74fbe6029ef64e00b751672bf478f1da866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016369"
---
# <a name="cmediasamplesetmediatime-method"></a>Metodo CMediaSample.SetMediaTime

Il `SetMediaTime` metodo imposta gli orari dei supporti per questo esempio. Questo metodo implementa il [**metodo IMediaSample::SetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntatore all'ora di inizio del supporto o **NULL.**

</dd> <dt>

*Pend* 
</dt> <dd>

Puntatore all'ora di arresto del supporto oppure **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

L'ora di arresto del supporto deve essere maggiore dell'ora di inizio del supporto. Usare **NULL per** invalidare i tempi dei supporti.

Il *parametro pEnd* specifica un tempo multimediale assoluto, ma la variabile membro [**CMediaSample::m \_ MediaEnd**](cmediasample-m-mediaend.md) viene calcolata come offset da *pStart*. In altre parole, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

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

 

 




