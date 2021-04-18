---
description: "Il metodo GetAvailable recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking:: GetAvailable."
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Metodo CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329045"
---
# <a name="csourceseekinggetavailable-method"></a>Metodo CSourceSeeking. GetAvailable

Il `GetAvailable` metodo recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEarliest* 
</dt> <dd>

Puntatore a una variabile che riceve la prima ora per una ricerca efficiente. La variabile è impostata su zero.

</dd> <dt>

*Piatto* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente. La variabile è impostata sul valore della variabile membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




