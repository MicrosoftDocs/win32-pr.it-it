---
description: Il metodo CallWorker segnala al thread la richiesta.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Metodo CAMThread. CallWorker (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331461"
---
# <a name="camthreadcallworker-method"></a>CAMThread. CallWorker, metodo

Il `CallWorker` metodo segnala al thread la richiesta.

## <a name="syntax"></a>Sintassi


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwParam* 
</dt> <dd>

Parametro della richiesta. La classe derivata definisce il significato del parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore definito dalla classe derivata.

## <a name="remarks"></a>Commenti

I metodi [**CAMThread:: GetRequest**](camthread-getrequest.md) e [**CAMThread:: CheckRequest**](camthread-checkrequest.md) recuperano il valore del parametro *dwParam* . Il metodo GetRequest si blocca fino a quando non `CallWorker` viene chiamato il metodo.

Questo metodo si blocca fino a quando non viene chiamato il metodo [**CAMThread:: Reply**](camthread-reply.md) . Il valore restituito è il parametro assegnato a Reply.

Questo metodo include il blocco [**CAMThread:: m \_ AccessLock**](camthread-m-accesslock.md) per serializzare le richieste. Pertanto, chiamare questo metodo dal thread stesso o da qualsiasi funzione membro eseguita nel contesto del thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




