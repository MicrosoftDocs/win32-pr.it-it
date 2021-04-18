---
description: 'Il metodo GetPin recupera un PIN. Questo metodo implementa il metodo CBaseFilter:: GetPin virtuale puro.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Metodo CSource. GetPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326936"
---
# <a name="csourcegetpin-method"></a>CSource. GetPin, metodo

Il `GetPin` metodo recupera un PIN. Questo metodo implementa il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) virtuale puro.

## <a name="syntax"></a>Sintassi


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero del PIN specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il puntatore all'oggetto [**CBasePin**](cbasepin.md) che implementa il PIN oppure **null** se l'indice non è compreso nell'intervallo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




