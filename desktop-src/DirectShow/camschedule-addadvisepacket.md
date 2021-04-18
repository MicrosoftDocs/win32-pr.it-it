---
description: Il metodo AddAdvisePacket aggiunge una richiesta di notifica all'elenco di richieste in sospeso.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Metodo CAMSchedule. AddAdvisePacket (Dsschedule. h)
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
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329572"
---
# <a name="camscheduleaddadvisepacket-method"></a>CAMSchedule. AddAdvisePacket, metodo

Il `AddAdvisePacket` metodo aggiunge una richiesta di notifica all'elenco di richieste in sospeso.

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

Tempo richiesto per l'avviso.

</dd> <dt>

*time2* \[ Ref\]
</dt> <dd>

Per richieste di notifica periodiche, tempo tra le notifiche. Questo parametro viene ignorato se *bPeriodic* è **false**.

</dd> <dt>

*hNotify* 
</dt> <dd>

Handle per un semaforo se *bPeriodic* è **true** oppure handle a un evento se *bPeriodic* è **false**.

</dd> <dt>

*bPeriodic* 
</dt> <dd>

Valore booleano che specifica se aggiungere una notifica periodica o una notifica monouso. Se **true**, la notifica è periodica; il parametro *time2* specifica l'intervallo tra le notifiche. Se **false**, la notifica viene eseguita una sola volta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un identificatore per la richiesta di notifica (il "cookie"). Se il metodo ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule. h (include Streams. h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




