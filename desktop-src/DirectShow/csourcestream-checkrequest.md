---
description: Il metodo CheckRequest controlla se è presente una richiesta di thread, senza blocco.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Metodo CSourceStream.CheckRequest (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bb77358ec579415439c2832b00255e7ffeb3c7eba0e387bfa0522a4a5109669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073315"
---
# <a name="csourcestreamcheckrequest-method"></a>Metodo CSourceStream.CheckRequest

Il `CheckRequest` metodo controlla se è presente una richiesta di thread, senza blocco.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCom* 
</dt> <dd>

Puntatore a una variabile che riceve il valore passato nell'ultima chiamata al [**metodo CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** è presente una richiesta in sospeso oppure FALSE in **caso** contrario.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CAMThread::CheckRequest**](camthread-checkrequest.md) per eseguire il controllo del tipo. La **classe CSourceStream** definisce il tipo enumerato seguente per il *parametro pCom:*


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

 

 




