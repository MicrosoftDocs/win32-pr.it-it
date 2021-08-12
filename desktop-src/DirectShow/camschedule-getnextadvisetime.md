---
description: Il metodo GetNextAdviseTime recupera l'ora della richiesta di consulenza successiva.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Metodo CAMSchedule.GetNextAdviseTime (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c7fd04622a5cdab8bade32f41b090d8f480db292209d284804b5180134954f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662347"
---
# <a name="camschedulegetnextadvisetime-method"></a>Metodo CAMSchedule.GetNextAdviseTime

Il `GetNextAdviseTime` metodo recupera l'ora della richiesta di consulenza successiva.

## <a name="syntax"></a>Sintassi


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce l'ora di riferimento della richiesta di consulenza successiva oppure MAX \_ TIME nessuna richiesta è pianificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule.h (includere Flussi.h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




