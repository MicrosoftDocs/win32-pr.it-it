---
description: Il metodo Close attende l'uscita del thread e quindi rilascia le relative risorse.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Metodo CAMThread.Close (Wxutil.h)
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
ms.openlocfilehash: bf12a80cd967832755f476db0e8810867326e84598ddce835e1da10dc6943419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158932"
---
# <a name="camthreadclose-method"></a>Metodo CAMThread.Close

Il `Close` metodo attende l'uscita del thread e quindi rilascia le relative risorse.

## <a name="syntax"></a>Sintassi


```C++
void Close();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario fornire un modo per la chiusura del thread. Ad esempio, nel metodo [**CAMThread::ThreadProc**](camthread-threadproc.md) definire una richiesta che segnali l'uscita del thread. Chiamare quindi il [**metodo CAMThread::CallWorker**](camthread-callworker.md) con tale valore.

Il metodo del distruttore [**~ CAMThread**](camthread--camthread.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




