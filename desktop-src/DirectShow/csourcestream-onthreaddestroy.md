---
description: Il metodo OnThreadDestroy viene chiamato quando il thread di streaming sta per uscire.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Metodo CSourceStream. OnThreadDestroy (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330038"
---
# <a name="csourcestreamonthreaddestroy-method"></a>CSourceStream. OnThreadDestroy, metodo

Il `OnThreadDestroy` metodo viene chiamato quando il thread di streaming sta per uscire.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

La routine thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chiama questo metodo prima di uscire. Il metodo non esegue alcuna operazione nella classe di base. è disponibile per la classe derivata di cui eseguire l'override. Se la classe derivata restituisce un codice di errore, il thread viene chiuso con un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




