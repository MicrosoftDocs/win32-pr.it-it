---
description: Il metodo get \_ Rate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaPosition::get \_ Rate.
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: CPosPassThru.get_Rate metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa8014d23bc488b4f0b8b0cc9b872dfdf4a56cced396cc22eefab5912df1706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073536"
---
# <a name="cpospassthruget_rate-method"></a>Metodo CPosPassThru.get \_ Rate

Il `get_Rate` metodo recupera la velocità di riproduzione. Questo metodo implementa il [**metodo IMediaPosition::get \_ Rate.**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Rate(
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

 

 




