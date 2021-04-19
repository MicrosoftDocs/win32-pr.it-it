---
description: Il metodo GetDueCommand recupera un puntatore al comando successivo che è dovuto a.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Metodo CCmdQueue. GetDueCommand (Winutil. h)
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
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324481"
---
# <a name="ccmdqueuegetduecommand-method"></a>CCmdQueue. GetDueCommand, metodo

Il `GetDueCommand` metodo recupera un puntatore al comando successivo che è dovuto a.

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

Tempo di attesa prima dell'esecuzione del timeout.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ Interrompi se si verifica un timeout. Restituisce \_ OK se ha esito positivo; in caso contrario, restituisce un errore. Restituisce un oggetto che è stato incrementato utilizzando **IUnknown:: AddRef**.

## <a name="remarks"></a>Commenti

Questa funzione membro si blocca fino a quando non è previsto un comando in sospeso. La funzione membro blocca per la quantità di tempo, in millisecondi, specificata nel parametro *msTimeout* . I comandi in fase di flusso diventano dovuti solo tra le funzioni membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) . Il comando rimane in coda fino a quando non viene eseguito o annullato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




