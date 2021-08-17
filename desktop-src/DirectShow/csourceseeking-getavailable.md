---
description: "Metodo CSourceSeeking.GetAvailable: il metodo GetAvailable recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking::GetAvailable."
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Metodo CSourceSeeking.GetAvailable (Ctlutil.h)
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
ms.openlocfilehash: ae42efad42bf9f1e0df0f4f791f1e4e8abb76fe8252818a8e35eda4dd6e6b87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953750"
---
# <a name="csourceseekinggetavailable-method"></a>Metodo CSourceSeeking.GetAvailable

Il `GetAvailable` metodo recupera l'intervallo di volte in cui la ricerca è efficiente. Questo metodo implementa il [**metodo IMediaSeeking::GetAvailable.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)

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

Puntatore a una variabile che riceve il primo tempo per una ricerca efficiente. La variabile è impostata su zero.

</dd> <dt>

*pLatest* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente. La variabile è impostata sul valore della variabile [**membro CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




