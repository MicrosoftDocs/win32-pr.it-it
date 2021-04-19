---
description: Il metodo Disconnect interrompe la connessione al pin corrente. Questo metodo implementa il metodo IPin::D la connessione.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Metodo CDynamicOutputPin. Disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331790"
---
# <a name="cdynamicoutputpindisconnect-method"></a>Metodo CDynamicOutputPin. Disconnect

Il `Disconnect` metodo interrompe la connessione al pin corrente. Questo metodo implementa il metodo [**Ipin::D la connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il PIN non era connesso.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                   |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBasePin::D la connessione**](cbasepin-disconnect.md) per abilitare la disconnessione mentre il filtro è attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




