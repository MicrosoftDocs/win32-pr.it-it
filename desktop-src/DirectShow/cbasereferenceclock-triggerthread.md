---
description: Il metodo TriggerThread attiva il thread di lavoro che gestisce la pianificazione.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Metodo CBaseReferenceClock.TriggerThread (Refclock.h)
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
ms.openlocfilehash: a8b53af246e029b5142b68840cfde0e776208e3c51093438042dd74f42a1b3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076441"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>Metodo CBaseReferenceClock.TriggerThread

Il `TriggerThread` metodo riattiva il thread di lavoro che gestisce la pianificazione.

## <a name="syntax"></a>Sintassi


```C++
void TriggerThread();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'orologio usa un thread di lavoro che chiama il [**metodo CAMSchedule::Advise**](camschedule-advise.md) nei momenti appropriati. La classe derivata può `TriggerThread` chiamare per riattivare il thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




