---
description: Il metodo GetPin recupera un segnaposto. Questo metodo implementa il metodo CBaseFilter::GetPin virtuale puro.
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Metodo CSource.GetPin (Source.h)
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
ms.openlocfilehash: 4c5b7548eca20f9ec6d9e03d0e708ead1b106f543ca8cac108700c64c9352ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087081"
---
# <a name="csourcegetpin-method"></a>Metodo CSource.GetPin

Il `GetPin` metodo recupera un segnaposto. Questo metodo implementa il metodo [**CBaseFilter::GetPin**](cbasefilter-getpin.md) virtuale puro.

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

Numero del pin specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il puntatore [**all'oggetto CBasePin**](cbasepin.md) che implementa il pin oppure **NULL** se l'indice non è compreso nell'intervallo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




