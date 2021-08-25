---
description: Il metodo OnThreadCreate viene chiamato quando viene inizializzato il thread di streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Metodo CSourceStream.OnThreadCreate (Source.h)
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
ms.openlocfilehash: 6e263f0ae72838504ab6d219c71d7841291a3edd2a7d6b719d112c74fb30c23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907711"
---
# <a name="csourcestreamonthreadcreate-method"></a>Metodo CSourceStream.OnThreadCreate

Il `OnThreadCreate` metodo viene chiamato quando viene inizializzato il thread di streaming.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

La routine del [**thread, CSourceStream::ThreadProc,**](csourcestream-threadproc.md)chiama questo metodo quando riceve per la prima volta una richiesta [**CSourceStream::Init.**](csourcestream-init.md) Il metodo non esegue alcuna operazione nella classe di base. La classe derivata può eseguire l'override di questo metodo per eseguire le inizializzazioni dei thread. Se la classe derivata restituisce un codice di errore, il thread viene chiuso con un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




