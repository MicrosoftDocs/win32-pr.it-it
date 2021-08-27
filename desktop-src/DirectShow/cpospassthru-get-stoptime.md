---
description: Il metodo get \_ StopTime recupera l'ora in cui la riproduzione verrà interrotta, in relazione alla durata del flusso. Questo metodo implementa il metodo IMediaPosition::get \_ StopTime.
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: CPosPassThru.get_StopTime metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea233d7e3a148088edd0f6963f45aeb0b483b41317481a95733fdc73c242027d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108301"
---
# <a name="cpospassthruget_stoptime-method"></a>Metodo CPosPassThru.get \_ StopTime

Il `get_StopTime` metodo recupera l'ora in cui la riproduzione verrà interrotta, in relazione alla durata del flusso. Questo metodo implementa il [**metodo IMediaPosition::get \_ StopTime.**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di arresto, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




