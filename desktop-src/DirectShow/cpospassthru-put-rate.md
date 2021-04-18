---
description: Il \_ metodo Put rate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaPosition::p UT \_ rate.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Metodo CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324181"
---
# <a name="cpospassthruput_rate-method"></a>Metodo di frequenza CPosPassThru. put \_

Il `put_Rate` metodo imposta la velocità di riproduzione. Questo metodo implementa il metodo [**IMediaPosition::p UT \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Rate(
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

Restituisce E \_ INVALIDARG se *drate* è zero. In caso contrario, restituisce il valore **HRESULT** dal pin connesso.

## <a name="remarks"></a>Commenti

Le frequenze negative indicano la riproduzione inversa. Non tutti i supporti supporteranno la riproduzione inversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




