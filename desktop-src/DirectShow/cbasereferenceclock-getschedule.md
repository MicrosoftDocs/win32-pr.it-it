---
description: Il metodo GetSchedule recupera un puntatore all'oggetto di pianificazione dell'orologio.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Metodo CBaseReferenceClock.GetSchedule (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6be5c4ed76573428967138682b478a54859e4ca97213f132ff805a0e83be0b50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822837"
---
# <a name="cbasereferenceclockgetschedule-method"></a>Metodo CBaseReferenceClock.GetSchedule

Il `GetSchedule` metodo recupera un puntatore all'oggetto di pianificazione dell'orologio.

## <a name="syntax"></a>Sintassi


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la variabile membro [**CBaseReferenceClock::m \_ pSchedule.**](cbasereferenceclock-m-pschedule.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




