---
description: Il metodo OnThreadCreate viene chiamato quando viene inizializzato il thread di streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Metodo CSourceStream. OnThreadCreate (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330041"
---
# <a name="csourcestreamonthreadcreate-method"></a>CSourceStream. OnThreadCreate, metodo

Il `OnThreadCreate` metodo viene chiamato quando viene inizializzato il thread di streaming.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

La routine thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chiama questo metodo quando riceve prima una richiesta [**CSourceStream:: init**](csourcestream-init.md) . Il metodo non esegue alcuna operazione nella classe di base. La classe derivata può eseguire l'override di questo metodo per eseguire le inizializzazioni dei thread. Se la classe derivata restituisce un codice di errore, il thread viene chiuso con un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




