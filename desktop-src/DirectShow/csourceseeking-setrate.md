---
description: 'Metodo CSourceSeeking.SetRate: il metodo SetRate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Metodo CSourceSeeking.SetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098739"
---
# <a name="csourceseekingsetrate-method"></a>Metodo CSourceSeeking.SetRate

Il `SetRate` metodo imposta la velocità di riproduzione. Questo metodo implementa il [**metodo IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dRate* 
</dt> <dd>

Velocità di riproduzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo aggiorna il valore della variabile membro [**CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) e quindi chiama il metodo virtuale puro [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md). Il metodo non convalida il *parametro dRate.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




