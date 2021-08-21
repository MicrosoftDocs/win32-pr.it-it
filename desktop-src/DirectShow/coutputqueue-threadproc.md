---
description: Il metodo ThreadProc recupera gli esempi dalla coda e li recapita al pin di input.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Metodo COutputQueue.ThreadProc (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d37158d71a74726e9bf27e76ffedb076f99b7380ffcca4edfa95928767eedbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073635"
---
# <a name="coutputqueuethreadproc-method"></a>Metodo COutputQueue.ThreadProc

Il `ThreadProc` metodo recupera gli esempi dalla coda e li recapita al pin di input.

## <a name="syntax"></a>Sintassi


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

Il [**metodo COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) chiama questo metodo, che implementa il ciclo del thread principale. All'interno del ciclo, il metodo esegue i passaggi seguenti:

1.  Recupera un esempio per la coda.
2.  Se l'esempio è un messaggio di controllo, il thread esegue l'azione di controllo. In caso contrario, inserisce l'esempio [**nella matrice COutputQueue::m \_ ppSamples.**](coutputqueue-m-ppsamples.md)
3.  Quando la matrice è piena (o se [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) è **FALSE),** il thread chiama il metodo [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) per distribuire gli esempi.
4.  Se non vengono accodati campioni, il thread attende il semaforo [**\_ HSem COutputQueue::m.**](coutputqueue-m-hsem.md)

Il thread termina quando la variabile membro [**COutputQueue::m \_ bTerminate**](coutputqueue-m-bterminate.md) diventa **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




