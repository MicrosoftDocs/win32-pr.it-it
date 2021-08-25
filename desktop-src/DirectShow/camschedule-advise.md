---
description: Il metodo Advise invia tutte le richieste pianificate per un orario specificato o una versione precedente.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Metodo CAMSchedule.Advise (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0943479aaa7fe2e6d699bba147977a73f48fc31186fb64ea26a211e2ea31d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757791"
---
# <a name="camscheduleadvise-method"></a>Metodo CAMSchedule.Advise

Il `Advise` metodo invia tutte le richieste pianificate per un orario specificato o una versione precedente.

## <a name="syntax"></a>Sintassi


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtTime* \[ Ref\]
</dt> <dd>

Valore che specifica l'ora di riferimento corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ora di riferimento della successiva richiesta di consulenza pianificata oppure MAX TIME se \_ non ne è rimasto nessuno.

## <a name="remarks"></a>Commenti

Quando l'orologio chiama questo metodo, specifica l'ora di riferimento corrente. L'utilità di pianificazione determina quali richieste di consulenza sono scadute, se presenti, e le invia. Se una richiesta con una sola operazione scade, l'utilità di pianificazione la elimina. Se una richiesta periodica scade, l'utilità di pianificazione la pianifica nuovamente per la successiva consulenza. Il metodo restituisce l'ora della richiesta in sospeso successiva.

Per inviare una richiesta di consulenza, l'utilità di pianificazione segnala l'evento o il semaforo specificato nel parametro *hNotify* del metodo [**CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule.h (includere Flussi.h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




