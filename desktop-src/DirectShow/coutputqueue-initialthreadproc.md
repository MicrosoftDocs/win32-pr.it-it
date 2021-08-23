---
description: Il metodo InitialThreadProc chiama il metodo COutputQueue::ThreadProc quando viene creato il thread.
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Inimetodo tialThreadProc (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a80561ae652df7168ad09c1cf6e9fde767154e6c72a8fe5360a5d09c784941f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813591"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Inimetodo tialThreadProc

Il `InitialThreadProc` metodo chiama il metodo [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) quando viene creato il thread.

## <a name="syntax"></a>Sintassi


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Puntatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore restituito dal [**metodo COutputQueue::ThreadProc.**](coutputqueue-threadproc.md)

## <a name="remarks"></a>Commenti

Questo metodo è la procedura di thread per il thread di lavoro dell'oggetto. Il puntatore `this` dell'oggetto è il parametro thread. Il metodo dereferenzia l'oggetto per chiamare **ThreadProc**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




