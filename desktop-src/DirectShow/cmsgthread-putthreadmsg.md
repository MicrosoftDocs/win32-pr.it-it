---
description: Accoda una richiesta di esecuzione da parte del thread di lavoro.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Metodo CMsgThread.PutThreadMsg (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7eefa95c4fd6ab19c895b4d1d47dba3a19302023985a4631708c3cf7ccc10d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585641"
---
# <a name="cmsgthreadputthreadmsg-method"></a>Metodo CMsgThread.PutThreadMsg

Accoda una richiesta di esecuzione da parte del thread di lavoro.

## <a name="syntax"></a>Sintassi


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Umsg* 
</dt> <dd>

Richiedere il codice.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Parametro flags facoltativo.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Puntatore facoltativo a un blocco di dati contenente parametri aggiuntivi o valori restituiti. Deve essere allocato in modo statico o heap e non automatico.

</dd> <dt>

*Pevent* 
</dt> <dd>

Puntatore facoltativo a un oggetto evento da segnalare al completamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro accoda una richiesta di esecuzione da parte del thread di lavoro. I parametri di questa funzione membro verranno accodati (in un oggetto [**CMsg)**](cmsg.md) e passati alla funzione membro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) del thread di lavoro. Questa funzione membro restituisce immediatamente dopo l'accodamento della richiesta e non attende che il thread adempia la richiesta. La **funzione membro CMsgThread::ThreadMessageProc** della classe derivata definisce i quattro parametri.

Questa funzione membro usa un elenco di thread sicuri multithread, pertanto è possibile effettuare più chiamate a questa funzione membro da thread diversi in modo sicuro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




