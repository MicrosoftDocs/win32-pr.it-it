---
description: Il metodo GetCommandDueFor recupera un comando posticipato pianificato a un'ora specificata.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Metodo CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324483"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>CCmdQueue. GetCommandDueFor, metodo

Il `GetCommandDueFor` metodo recupera un comando posticipato pianificato a un'ora specificata.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStream* 
</dt> <dd>

Ora pianificata per il comando.

</dd> <dt>

*ppCmd* 
</dt> <dd>

Indirizzo di un puntatore al comando posticipato da eseguire al momento specificato nel parametro *tStream* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E \_ non \_ trovato se nessun comando è dovuto; in caso contrario, restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questa funzione membro accetta un flusso di tempo e restituisce il comando posticipato pianificato in quel momento. L'offset del tempo effettivo del flusso viene calcolato quando viene eseguita la coda dei comandi. I comandi rimangono accodati fino all'esecuzione o annullati. Questa funzione membro non verrà bloccata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




