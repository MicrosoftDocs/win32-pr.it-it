---
description: Si blocca fino alla chiusura del thread.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Metodo CMsgThread.WaitForThreadExit (Msgthrd.h)
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
ms.openlocfilehash: de9861a1c7cae3055be288c4624b9e0b98c7b719e1534c1841ddb17770d91cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915711"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>Metodo CMsgThread.WaitForThreadExit

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

Restituisce **TRUE** o **FALSE,** il cui significato è determinato dalla classe che fornisce la funzione membro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) sottoposta a override e la funzione membro chiamante.

## <a name="remarks"></a>Commenti

Assicurarsi che il thread di lavoro sia stato chiuso completamente prima di completare l'eliminazione della classe derivata. In caso contrario, il thread potrebbe comunque essere eseguito dopo lo scaricamento della libreria a collegamento dinamico (DLL) dallo spazio indirizzi del processo. Anche se l'unica istruzione da uscire è un'istruzione a restituzione singola, verrà generata un'eccezione. L'unico modo affidabile per assicurarsi che il thread sia terminato è segnalare l'uscita del thread (usando un oggetto [**CMsg**](cmsg.md) negoziato privatamente inviato alla funzione membro [**CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) e quindi chiamare questa funzione membro. È necessario eseguire questa operazione nel distruttore per la classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




