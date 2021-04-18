---
description: Il \_ metodo Put PrerollTime imposta la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo IMediaPosition::p UT \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Metodo CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329757"
---
# <a name="cpospassthruput_prerolltime-method"></a>CPosPassThru. put \_ PrerollTime (metodo)

Il `put_PrerollTime` metodo imposta la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo [**IMediaPosition::p UT \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*llTime* 
</dt> <dd>

Tempo di preiscrizione, in secondi.

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

 

 




