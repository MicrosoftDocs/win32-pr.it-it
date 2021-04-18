---
description: Restituisce TRUE se il thread corrente è il proprietario della sezione critica specificata.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Funzione CritCheckIn (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327190"
---
# <a name="critcheckin-function"></a>CritCheckIn (funzione)

Restituisce **true** se il thread corrente è il proprietario della sezione critica specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntatore a una sezione critica [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nelle compilazioni di debug, restituisce **true** se il thread corrente è il proprietario di questa sezione critica o **false** in caso contrario. Nelle compilazioni finali restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Questa funzione è particolarmente utile all'interno della macro [**Assert**](assert.md) per verificare se un thread è proprietario di un determinato blocco.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come utilizzare questa funzione:


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug della sezione critica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




