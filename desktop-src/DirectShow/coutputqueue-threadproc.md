---
description: Il metodo ThreadProc recupera campioni dalla coda e li recapita al pin di input.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Metodo COutputQueue. ThreadProc (Outputq. h)
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
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324669"
---
# <a name="coutputqueuethreadproc-method"></a>COutputQueue. ThreadProc, metodo

Il `ThreadProc` metodo recupera campioni dalla coda e li recapita al pin di input.

## <a name="syntax"></a>Sintassi


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

Il metodo [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md) chiama questo metodo, che implementa il ciclo del thread principale. All'interno del ciclo, il metodo esegue i passaggi seguenti:

1.  Recupera un esempio per la coda.
2.  Se l'esempio è un messaggio di controllo, il thread esegue l'azione di controllo. In caso contrario, inserisce l'esempio nella matrice [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .
3.  Quando la matrice è completa (o se [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) è **false**), il thread chiama il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) per recapitare gli esempi.
4.  Se nessun campione viene accodato, il thread resta in attesa sul semaforo [**COutputQueue:: m \_ hSem**](coutputqueue-m-hsem.md) .

Il thread termina quando la variabile membro [**COutputQueue:: m \_ BTerminate**](coutputqueue-m-bterminate.md) diventa **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




