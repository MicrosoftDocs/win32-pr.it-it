---
description: Il metodo put \_ CurrentPosition imposta la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaPosition::p ut \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: CPosPassThru.put_CurrentPosition metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab6a8323023e9a2cd20f9453dc00e0c56a688086f10772b72b59b3c012a24702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909221"
---
# <a name="cpospassthruput_currentposition-method"></a>Metodo CPosPassThru.put \_ CurrentPosition

Il `put_CurrentPosition` metodo imposta la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il [**metodo IMediaPosition::p ut \_ CurrentPosition.**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition)

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*llTime* 
</dt> <dd>

Nuova posizione, in secondi.

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

 

 




