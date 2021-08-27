---
description: "Metodo CPosPassThru.GetAvailable: il metodo GetAvailable recupera l'intervallo di volte in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking::GetAvailable."
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Metodo CPosPassThru.GetAvailable (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1db45b20264f192b2ade7d8863f9da86d5fc02159567611eff86e9cdfff1b10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084251"
---
# <a name="cpospassthrugetavailable-method"></a>Metodo CPosPassThru.GetAvailable

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

Puntatore a una variabile che riceve l'ora meno recente per una ricerca efficiente.

</dd> <dt>

*pLatest* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




