---
description: Crea un thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Metodo CMsgThread. CreateThread (Msgthrd. h)
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
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328834"
---
# <a name="cmsgthreadcreatethread-method"></a>CMsgThread. CreateThread, metodo

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
| <dl> <dt>TRUE * * * *</dt> </dl>  | Creazione thread completata.<br/>     |
| <dl> <dt>FALSE * * * *</dt> </dl> | Creazione del thread non riuscita.<br/> |



 

## <a name="remarks"></a>Commenti

Il thread effettuerà il ciclo, bloccando la coda di una richiesta (tramite la funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e quindi chiamando la funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) con ogni messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




