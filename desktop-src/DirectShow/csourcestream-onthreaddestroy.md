---
description: Il metodo OnThreadDestroy viene chiamato quando il thread di streaming sta per uscire.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Metodo CSourceStream.OnThreadDestroy (Source.h)
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
ms.openlocfilehash: b71bd7ff9da79ed42ad7d36ff176a60687ca5fd0edcd6003d77c20084adc1b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953700"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Metodo CSourceStream.OnThreadDestroy

Il `OnThreadDestroy` metodo viene chiamato quando il thread di streaming sta per uscire.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

La routine del [**thread, CSourceStream::ThreadProc,**](csourcestream-threadproc.md)chiama questo metodo prima della chiusura. Il metodo non esegue alcuna operazione nella classe di base. è disponibile per la classe derivata di cui eseguire l'override. Se la classe derivata restituisce un codice di errore, il thread viene chiuso con un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




