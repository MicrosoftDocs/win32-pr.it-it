---
description: 'Il metodo serate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: SetValue.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Metodo CSourceSeeking. serate (Ctlutil. h)
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
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328483"
---
# <a name="csourceseekingsetrate-method"></a>CSourceSeeking. serate (metodo)

Il `SetRate` metodo imposta la velocità di riproduzione. Questo metodo implementa il metodo [**IMediaSeeking::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) SetValue.

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

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo aggiorna il valore della variabile membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) e quindi chiama il metodo virtuale pure [**CSourceSeeking:: changerate**](csourceseeking-changerate.md). Il metodo non convalida il parametro *drate* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




