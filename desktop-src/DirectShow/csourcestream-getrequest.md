---
description: Il metodo GetRequest attende la richiesta del thread successivo.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Metodo CSourceStream.GetRequest (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e28a8e57535a49903cd2a7b23fb0d0d179bf910b20225042c65b3bdcda620f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073205"
---
# <a name="csourcestreamgetrequest-method"></a>Metodo CSourceStream.GetRequest

Il `GetRequest` metodo attende la richiesta del thread successivo.

## <a name="syntax"></a>Sintassi


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la richiesta di thread successiva.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CAMThread::GetRequest.**](camthread-getrequest.md) Viene eseguito il cast del valore restituito al tipo enumerato seguente:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




