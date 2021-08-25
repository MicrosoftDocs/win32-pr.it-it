---
description: Il metodo CurrentStopTime recupera l'ora di arresto del segmento, impostata dal metodo CBasePin::NewSegment.
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Metodo CBasePin.CurrentStopTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2905913828c91fffde9fb474802c8dea0e0f83d59ccdb5408f846a1936071cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916701"
---
# <a name="cbasepincurrentstoptime-method"></a>Metodo CBasePin.CurrentStopTime

Il `CurrentStopTime` metodo recupera il tempo di arresto del segmento, impostato dal metodo [**CBasePin::NewSegment.**](cbasepin-newsegment.md)

## <a name="syntax"></a>Sintassi


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore di [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




