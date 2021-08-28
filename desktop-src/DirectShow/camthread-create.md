---
description: Il metodo Create crea il thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Metodo CAMThread.Create (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 135af6dd12bb53a2fa1e7ec14425c12e1c0bcc99bf9c82ce7aeaccb72df544f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103321"
---
# <a name="camthreadcreate-method"></a>Metodo CAMThread.Create

Il `Create` metodo crea il thread.

## <a name="syntax"></a>Sintassi


```C++
BOOL Create();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo crea il thread usando il metodo [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) per la routine del thread e `this` per l'argomento thread.

Il metodo ha esito negativo se il thread esiste già.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




