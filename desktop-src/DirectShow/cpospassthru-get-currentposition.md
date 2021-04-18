---
description: 'Il \_ metodo Get CurrentPosition recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaPosition:: Get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Metodo CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327441"
---
# <a name="cpospassthruget_currentposition-method"></a>Metodo CPosPassThru. Get \_ currentPosition

Il `get_CurrentPosition` metodo recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo [**IMediaPosition:: Get \_ currentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione corrente, in secondi.

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

 

 




