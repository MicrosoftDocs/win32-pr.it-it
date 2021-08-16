---
description: Il metodo Run esegue l'oggetto . Questo metodo implementa il metodo IMediaFilter::Run.
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Metodo CBaseMediaFilter.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 73ab65404b6946a1cf220db54789df1234e14bf815c44633d3237ab50e04e2e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823691"
---
# <a name="cbasemediafilterrun-method"></a>Metodo CBaseMediaFilter.Run

Il `Run` metodo esegue l'oggetto . Questo metodo implementa il [**metodo IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Ora di riferimento corrispondente all'ora del flusso 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Se l'oggetto viene arrestato, questo metodo sospende l'oggetto chiamando il metodo [**CBaseMediaFilter::P ause.**](cbasemediafilter-pause.md) Imposta quindi la variabile [**membro CBaseMediaFilter::m \_ State**](cbasemediafilter-m-state.md) su State \_ Running.

L'ora del flusso viene calcolata come ora di riferimento corrente meno *tStart*. È necessario eseguire il rendering di un campione multimediale con timestamp pari a zero all'ora *tStart*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




