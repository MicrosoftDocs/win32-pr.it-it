---
description: Il metodo Reply risponde a una richiesta.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Metodo CAMThread. Reply (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332358"
---
# <a name="camthreadreply-method"></a>Metodo CAMThread. Reply

Il `Reply` metodo risponde a una richiesta.

## <a name="syntax"></a>Sintassi


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dw* 
</dt> <dd>

Valore da restituire nel metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo CallWorker si blocca fino a quando non viene chiamato questo metodo. Il parametro *DW* fornisce il valore restituito per CallWorker. Chiamare questo metodo nella routine del thread dopo aver recuperato una richiesta, per rilasciare il thread richiedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




