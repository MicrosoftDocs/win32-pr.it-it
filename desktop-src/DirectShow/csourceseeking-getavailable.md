---
description: "Metodo CSourceSeeking.GetAvailable: il metodo GetAvailable recupera l'intervallo di volte in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking::GetAvailable."
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
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085239"
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

Puntatore a una variabile che riceve l'ora meno recente per una ricerca efficiente. La variabile è impostata su zero.

</dd> <dt>

*pLatest* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente. La variabile è impostata sul valore della variabile membro [**CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




