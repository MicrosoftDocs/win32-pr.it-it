---
description: Il metodo GetRequest attende la richiesta del thread successivo.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Metodo CSourceStream. GetRequest (source. h)
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
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330048"
---
# <a name="csourcestreamgetrequest-method"></a>Metodo CSourceStream. GetRequest

Il `GetRequest` metodo attende la richiesta del thread successivo.

## <a name="syntax"></a>Sintassi


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la richiesta successiva del thread.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CAMThread:: GetRequest**](camthread-getrequest.md) . Viene eseguito il cast del valore restituito al tipo enumerato seguente:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




