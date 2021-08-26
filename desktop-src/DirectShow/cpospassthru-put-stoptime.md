---
description: Il metodo put \_ StopTime imposta l'ora in cui la riproduzione verrà interrotta, in relazione alla durata del flusso. Questo metodo implementa il metodo IMediaPosition::p ut \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: CPosPassThru.put_StopTime metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d91d49f2517a3d3b9efc50d70ace1b75562b50df8acda7c48826e7c088439928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055091"
---
# <a name="cpospassthruput_stoptime-method"></a>Metodo CPosPassThru.put \_ StopTime

Il `put_StopTime` metodo imposta l'ora in cui la riproduzione verrà interrotta, in relazione alla durata del flusso. Questo metodo implementa il [**metodo IMediaPosition::p ut \_ StopTime.**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime)

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*llTime* 
</dt> <dd>

Ora di arresto come **valore doppio,** in secondi.

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

 

 




