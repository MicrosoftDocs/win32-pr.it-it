---
description: Si blocca fino alla chiusura del thread.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Metodo CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330220"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>CMsgThread. WaitForThreadExit, metodo

Si blocca fino alla chiusura del thread.

## <a name="syntax"></a>Sintassi


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpdwExitCode* 
</dt> <dd>

Puntatore al codice di uscita restituito dal thread.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** o **false**, il cui significato è determinato dalla classe che fornisce la funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) sottoposta a override e la funzione membro chiamante.

## <a name="remarks"></a>Commenti

Verificare che il thread di lavoro sia stato chiuso completamente prima di completare la distruzione della classe derivata; in caso contrario, il thread potrebbe essere ancora eseguito dopo che la libreria di collegamento dinamico (DLL) è stata scaricata dallo spazio degli indirizzi del processo. Anche se l'unica istruzione lasciata per uscire è un'istruzione a singolo ritorno, si verificherà un'eccezione. L'unico modo affidabile per assicurarsi che il thread sia stato terminato consiste nel segnalare al thread di uscire (usando un oggetto [**CMsg**](cmsg.md) negoziato privatamente inviato alla funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e quindi chiamare questa funzione membro. Questa operazione deve essere eseguita nel distruttore per la classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




