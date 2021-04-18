---
description: "Il metodo GetRequestHandle recupera un handle per l'evento segnalato dal metodo CAMThread:: CallWorker."
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Metodo CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330860"
---
# <a name="camthreadgetrequesthandle-method"></a>CAMThread. GetRequestHandle, metodo

Il `GetRequestHandle` metodo recupera un handle per l'evento segnalato dal metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un handle di evento.

## <a name="remarks"></a>Commenti

La classe CAMEvent mantiene un evento di reimpostazione manuale privato, che viene impostato da CallWorker e reimpostato dal metodo [**CAMThread:: Reply**](camthread-reply.md) .

Se si chiama una funzione come WaitForMultipleObjects, utilizzare GetRequestHandle per recuperare l'handle dell'evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




