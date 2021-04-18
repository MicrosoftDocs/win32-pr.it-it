---
description: Il metodo Create crea il thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Metodo CAMThread. Create (Wxutil. h)
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
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330548"
---
# <a name="camthreadcreate-method"></a>Metodo CAMThread. Create

Il `Create` metodo crea il thread.

## <a name="syntax"></a>Sintassi


```C++
BOOL Create();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo crea il thread, usando il metodo [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) per la routine thread e `this` per l'argomento thread.

Il metodo ha esito negativo se il thread esiste già.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




