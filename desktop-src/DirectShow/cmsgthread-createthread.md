---
description: Crea un thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Metodo CMsgThread.CreateThread (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831871"
---
# <a name="cmsgthreadcreatethread-method"></a>Metodo CMsgThread.CreateThread

Crea un thread.

## <a name="syntax"></a>Sintassi


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                              | Descrizione                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>TRUE****</dt> </dl>  | Il thread è stato creato correttamente.<br/>     |
| <dl> <dt>FALSE****</dt> </dl> | Il thread non è stato creato correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Il thread verrà ciclico, bloccando fino a quando una richiesta non viene accodata (tramite la funzione membro [**CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) e quindi chiamando la funzione membro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) con ogni messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




