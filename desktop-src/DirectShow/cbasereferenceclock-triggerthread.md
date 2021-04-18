---
description: Il metodo TriggerThread attiva il thread di lavoro che gestisce la pianificazione.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Metodo CBaseReferenceClock. TriggerThread (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332219"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>CBaseReferenceClock. TriggerThread, metodo

Il `TriggerThread` metodo attiva il thread di lavoro che gestisce la pianificazione.

## <a name="syntax"></a>Sintassi


```C++
void TriggerThread();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il clock usa un thread di lavoro che chiama il metodo [**CAMSchedule:: Advise**](camschedule-advise.md) in momenti appropriati. La classe derivata può chiamare `TriggerThread` per riattivare il thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




