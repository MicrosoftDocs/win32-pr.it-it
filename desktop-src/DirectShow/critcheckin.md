---
description: Restituisce TRUE se il thread corrente è il proprietario della sezione critica specificata.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Funzione CritCheckIn (Wxutil.h)
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
ms.openlocfilehash: 4f4e9ff0078f6efe8dee9b060e61858c24aea0a64e7e35b9fb867125b8612ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908081"
---
# <a name="critcheckin-function"></a>Funzione CritCheckIn

Restituisce **TRUE** se il thread corrente è il proprietario della sezione critica specificata.

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

Puntatore a [**una sezione critica CCritSec.**](ccritsec.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nelle build di debug restituisce **TRUE se** il thread corrente è il proprietario di questa sezione critica oppure FALSE **in caso** contrario. Nelle build per la vendita al dettaglio, restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questa funzione è particolarmente utile all'interno della macro [**ASSERT**](assert.md) per verificare se un thread è proprietario di un determinato blocco.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra come usare questa funzione:


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
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug delle sezioni critiche](critical-section-debugging-functions.md)
</dt> </dl>

 

 




