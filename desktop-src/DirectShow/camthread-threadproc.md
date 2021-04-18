---
description: Il metodo ThreadProc è la routine thread.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Metodo CAMThread. ThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330543"
---
# <a name="camthreadthreadproc-method"></a>CAMThread. ThreadProc, metodo

Il `ThreadProc` metodo è la routine del thread.

## <a name="syntax"></a>Sintassi


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** il cui significato è definito dalla classe derivata.

## <a name="remarks"></a>Commenti

Si tratta di un metodo virtuale puro. Implementare questo metodo nella classe derivata per fornire una routine del thread. Quando il metodo [**CAMThread:: create**](camthread-create.md) crea un thread, fornisce l'indirizzo del metodo [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) , che a sua volta chiama il metodo ThreadProc.

In genere, il metodo ThreadProc entrerà in un ciclo che recupera le richieste (chiamando i metodi [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md) ) ed elabora i dati.

Quando questo metodo viene restituito, il thread viene chiuso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




