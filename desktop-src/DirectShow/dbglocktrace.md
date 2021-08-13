---
description: Abilita o disabilita la registrazione di debug di una determinata sezione critica.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Funzione DbgLockTrace (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b55736b2efb8fd4cfbca40710caa930c200c84e1ceec9c8c4f7439468c1add1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654071"
---
# <a name="dbglocktrace-function"></a>Funzione DbgLockTrace

Abilita o disabilita la registrazione di debug di una determinata sezione critica.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntatore a [**una sezione critica CCritSec.**](ccritsec.md)

</dd> <dt>

*fTrace* 
</dt> <dd>

Valore che specifica se la registrazione è abilitata. Usare **TRUE per** abilitare la registrazione o **FALSE** per disabilitarla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare questa funzione per tracciare una sezione critica specifica. Per impostazione predefinita, la registrazione di debug delle sezioni critiche è disabilitata a causa del numero elevato di sezioni critiche.

Per tracciare una sezione critica, seguire questa procedura:

1.  Definire DEBUG o \_ DEBUG prima di includere le intestazioni DirectShow.
2.  Abilitare la registrazione di debug per le sezioni critiche chiamando [**DbgSetModuleLevel con**](dbgsetmodulelevel.md) il flag LOG \_ LOCKING.
3.  Chiamare **DbgLockTrace** nella sezione critica da tracciare.

Nelle build per la vendita al dettaglio, **la funzione DbgLockTrace** non ha alcun effetto.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come tracciare una sezione critica.


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
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

 

 




