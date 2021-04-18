---
description: Il metodo Close attende la chiusura del thread, quindi rilascia le relative risorse.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Metodo CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331291"
---
# <a name="camthreadclose-method"></a>Metodo CAMThread. Close

Il `Close` metodo attende la chiusura del thread, quindi rilascia le relative risorse.

## <a name="syntax"></a>Sintassi


```C++
void Close();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario fornire un modo per uscire dal thread. Nel metodo [**CAMThread:: ThreadProc**](camthread-threadproc.md) , ad esempio, definire una richiesta che segnali la chiusura del thread. Chiamare quindi il metodo [**CAMThread:: CallWorker**](camthread-callworker.md) con tale valore.

Il metodo del distruttore [**~ CAMThread**](camthread--camthread.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




