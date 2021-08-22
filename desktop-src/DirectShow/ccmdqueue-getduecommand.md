---
description: Il metodo GetDueCommand recupera un puntatore al comando successivo dovuto.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Metodo CCmdQueue.GetDueCommand (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6e7c8d133537dc2b185c755e65f3a4febbee762c5c2306de37ad0c627434df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016429"
---
# <a name="ccmdqueuegetduecommand-method"></a>Metodo CCmdQueue.GetDueCommand

Il `GetDueCommand` metodo recupera un puntatore al comando successivo dovuto.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppCmd* 
</dt> <dd>

Indirizzo di un puntatore al comando posticipato.

</dd> <dt>

*msTimeout* 
</dt> <dd>

Tempo di attesa prima di effettuare il timeout.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ ABORT se si verifica un timeout. Restituisce S \_ OK in caso di esito positivo; in caso contrario, restituisce un errore. Restituisce un oggetto incrementato utilizzando **IUnknown::AddRef**.

## <a name="remarks"></a>Commenti

Questa funzione membro si blocca fino alla scadenza di un comando in sospeso. La funzione membro si blocca per la quantità di tempo, in millisecondi, specificata nel *parametro msTimeout.* I comandi in fase di flusso diventano dovuti solo tra le funzioni membro [**CCmdQueue::Run**](ccmdqueue-run.md) e [**CCmdQueue::EndRun.**](ccmdqueue-endrun.md) Il comando rimane in coda fino all'esecuzione o all'annullamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




