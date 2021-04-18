---
description: 'Il metodo getrate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: getrate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Metodo CPosPassThru. getrate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325512"
---
# <a name="cpospassthrugetrate-method"></a>CPosPassThru. getrate, metodo

Il `GetRate` metodo recupera la velocità di riproduzione. Questo metodo implementa il metodo [**IMediaSeeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdRate* 
</dt> <dd>

Puntatore a una variabile che riceve la velocità di riproduzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




