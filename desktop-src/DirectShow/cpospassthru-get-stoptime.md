---
description: "Il \\_ metodo Get StopTime recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso. Questo metodo implementa il metodo IMediaPosition:: Get \\_ StopTime."
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Metodo CPosPassThru.get_StopTime (Ctlutil. h)
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
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327540"
---
# <a name="cpospassthruget_stoptime-method"></a>Metodo CPosPassThru. Get \_ StopTime

Il `get_StopTime` metodo recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso. Questo metodo implementa il metodo [**IMediaPosition:: Get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .

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

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




