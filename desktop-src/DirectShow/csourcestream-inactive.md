---
description: Il metodo Inactive notifica al pin che il filtro non è più attivo. Questo metodo esegue l'override del metodo CBasePin::Inactive. Se il thread di streaming è attivo, questo metodo lo arresta e attende la chiusura del thread.
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Metodo CSourceStream.Inactive (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9d9424f4299d7a07ad98010846fa917307bd38eead028b4b8c38c40e2284c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687371"
---
# <a name="csourcestreaminactive-method"></a>Metodo CSourceStream.Inactive

Il `Inactive` metodo notifica al pin che il filtro non è più attivo. Questo metodo esegue l'override [**del metodo CBasePin::Inactive.**](cbasepin-inactive.md) Se il thread di streaming è attivo, questo metodo lo arresta e attende la chiusura del thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




