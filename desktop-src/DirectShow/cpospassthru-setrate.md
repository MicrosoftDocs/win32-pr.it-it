---
description: 'Metodo CPosPassThru.SetRate: il metodo SetRate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Metodo CPosPassThru.SetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c411f2c342bd54f89ac85ad4275a05e9d7854908c1d8ba88b1181f34e56f57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909071"
---
# <a name="cpospassthrusetrate-method"></a>Metodo CPosPassThru.SetRate

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

Velocità di riproduzione. Non deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ INVALIDARG se *dRate* è zero. In caso contrario, restituisce **il valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




