---
description: Il metodo Advise Invia tutte le richieste pianificate per un periodo di tempo specificato o un valore precedente.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Metodo CAMSchedule. Advise (Dsschedule. h)
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
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329571"
---
# <a name="camscheduleadvise-method"></a>Metodo CAMSchedule. Advise

Il `Advise` metodo invia tutte le richieste pianificate per un periodo di tempo specificato o un valore precedente.

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

Restituisce l'ora di riferimento della richiesta di notifica pianificata successiva o il \_ tempo massimo se non ne è rimasto alcuno.

## <a name="remarks"></a>Commenti

Quando il clock chiama questo metodo, specifica l'ora di riferimento corrente. L'utilità di pianificazione determina quali richieste di notifica sono scadute, se presenti, e le invia. Se una richiesta di una volta scade, l'utilità di pianificazione la Elimina. Se una richiesta periodica scade, l'utilità di pianificazione lo Ripianifica per il successivo tempo di notifica. Il metodo restituisce l'ora della richiesta in sospeso successiva.

Per inviare una richiesta di notifica, l'utilità di pianificazione segnala l'evento o il semaforo specificato nel parametro *hNotify* del metodo [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule. h (include Streams. h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




