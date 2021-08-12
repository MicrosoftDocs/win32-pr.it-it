---
description: Il metodo Reply risponde a una richiesta.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Metodo CAMThread.Reply (Wxutil.h)
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
ms.openlocfilehash: 9783703d711800b8002aa0372292349d83620eafb097be2256ffde6ab2c91c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662367"
---
# <a name="camthreadreply-method"></a>Metodo CAMThread.Reply

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

Valore da restituire nel [**metodo CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo CallWorker si blocca fino a quando non viene chiamato questo metodo. Il *parametro dw* fornisce il valore restituito per CallWorker. Chiamare questo metodo nella routine del thread dopo aver recuperato una richiesta per rilasciare il thread richiedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




