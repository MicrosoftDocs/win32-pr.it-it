---
description: Il metodo CurrentStartTime recupera l'ora di inizio del segmento, impostata dal metodo CBasePin::NewSegment.
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Metodo CBasePin.CurrentStartTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c92355b397736b713fcf5fd09a61a130761a0cb954331b606ec1367fd65e6e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916741"
---
# <a name="cbasepincurrentstarttime-method"></a>Metodo CBasePin.CurrentStartTime

Il `CurrentStartTime` metodo recupera l'ora di inizio del segmento, impostata dal [**metodo CBasePin::NewSegment.**](cbasepin-newsegment.md)

## <a name="syntax"></a>Sintassi


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CBasePin::m \_ tStart.**](cbasepin-m-tstart.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




