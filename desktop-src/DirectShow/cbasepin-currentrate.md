---
description: Il metodo CurrentRate recupera la frequenza dei segmenti, impostata dal metodo CBasePin::NewSegment.
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Metodo CBasePin.CurrentRate (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c522a76aebce39e4670d4d00b3344bf56d20172c2d54243322dd36a5d203226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955200"
---
# <a name="cbasepincurrentrate-method"></a>Metodo CBasePin.CurrentRate

Il `CurrentRate` metodo recupera la frequenza dei segmenti, impostata dal metodo [**CBasePin::NewSegment.**](cbasepin-newsegment.md)

## <a name="syntax"></a>Sintassi


```C++
double CurrentRate();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CBasePin::m \_ dRate**](cbasepin-m-drate.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




