---
description: "Il metodo attivo notifica al pin che il filtro è ora attivo. Questo metodo esegue l'override del Metodo CBasePin:: Active. Se il PIN è connesso, questo metodo avvia il thread di streaming."
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Metodo CSourceStream. Active (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329036"
---
# <a name="csourcestreamactive-method"></a>Metodo CSourceStream. Active

Il `Active` metodo notifica al pin che il filtro è ora attivo. Questo metodo esegue l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) . Se il PIN è connesso, questo metodo avvia il thread di streaming.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Il PIN è già attivo.<br/>  |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                    |
| <dl> <dt>**E \_ non riescono**</dt> </dl>  | Non è stato possibile avviare il thread.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




