---
description: Il metodo AddAdvisePacket aggiunge una richiesta di consulenza all'elenco delle richieste in sospeso.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Metodo CAMSchedule.AddAdvisePacket (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a7509e4696214279e99ff15f21f2634dce7921796ae2ca112ae563ab170a2d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084531"
---
# <a name="camscheduleaddadvisepacket-method"></a>Metodo CAMSchedule.AddAdvisePacket

Il `AddAdvisePacket` metodo aggiunge una richiesta di consulenza all'elenco di richieste in sospeso.

## <a name="syntax"></a>Sintassi


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*time1* \[ Ref\]
</dt> <dd>

Tempo richiesto per la consulenza.

</dd> <dt>

*time2* \[ Ref\]
</dt> <dd>

Per le richieste di consulenza periodiche, tempo tra le notifiche. Questo parametro viene ignorato se *bPeriodic* è **FALSE.**

</dd> <dt>

*hNotify* 
</dt> <dd>

Handle a un semaforo se *bPeriodic* è **TRUE** o handle a un evento se *bPeriodic* è **FALSE.**

</dd> <dt>

*bPeriodic* 
</dt> <dd>

Valore booleano che specifica se aggiungere una notifica periodica o una notifica con un'unica operazione. Se **TRUE,** la notifica è periodica. il *parametro time2* specifica il tempo tra le notifiche. Se **FALSE,** la notifica viene eseguita una sola volta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un identificatore per la richiesta di consulenza (il "cookie"). Se il metodo ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule.h (includere Flussi.h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




