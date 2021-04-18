---
description: Accoda una richiesta di esecuzione da parte del thread di lavoro.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Metodo CMsgThread. PutThreadMsg (Msgthrd. h)
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
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331290"
---
# <a name="cmsgthreadputthreadmsg-method"></a>CMsgThread. PutThreadMsg, metodo

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

*uMsg* 
</dt> <dd>

Codice della richiesta.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Parametro flags facoltativo.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Puntatore facoltativo a un blocco di dati contenente parametri o valori restituiti aggiuntivi. Deve essere allocato in modo statico o heap e non automatico.

</dd> <dt>

*pEvent* 
</dt> <dd>

Puntatore facoltativo a un oggetto evento da segnalare al completamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro accoda una richiesta di esecuzione da parte del thread di lavoro. I parametri di questa funzione membro verranno accodati (in un oggetto [**CMsg**](cmsg.md) ) e passati alla funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) del thread di lavoro. Questa funzione membro viene restituita immediatamente dopo l'accodamento della richiesta e non attende che il thread soddisfi la richiesta. La funzione membro **CMsgThread:: ThreadMessageProc** della classe derivata definisce i quattro parametri.

Questa funzione membro usa un elenco multithread safe, quindi è possibile rendere sicure più chiamate a questa funzione membro da thread diversi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




