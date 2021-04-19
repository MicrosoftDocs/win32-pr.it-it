---
description: 'Il \_ metodo get Duration recupera la durata del flusso. Questo metodo implementa il metodo IMediaPosition:: Get \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Metodo CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332578"
---
# <a name="cpospassthruget_duration-method"></a>Metodo CPosPassThru. Get \_ Duration

Il `get_Duration` metodo recupera la durata del flusso. Questo metodo implementa il metodo [**IMediaPosition:: Get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plength* 
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza totale del flusso, in secondi.

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

 

 




