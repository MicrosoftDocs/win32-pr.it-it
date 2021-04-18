---
description: Il metodo EndFlush termina un'operazione di svuotamento.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Metodo COutputQueue. EndFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330210"
---
# <a name="coutputqueueendflush-method"></a>COutputQueue. EndFlush, metodo

Il `EndFlush` metodo termina un'operazione di svuotamento.

## <a name="syntax"></a>Sintassi


```C++
void EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'oggetto utilizza un thread, questo metodo attende l'evento [**COutputQueue:: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) . Il thread segnala questo evento dopo aver liberato tutti gli esempi in sospeso. Se l'oggetto non utilizza un thread, questo metodo chiama il metodo [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) . Il `EndFlush` metodo chiama quindi il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




