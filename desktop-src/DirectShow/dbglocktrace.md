---
description: Abilita o Disabilita la registrazione di debug di una sezione critica specificata.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Funzione DbgLockTrace (Wxutil. h)
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
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327525"
---
# <a name="dbglocktrace-function"></a>DbgLockTrace (funzione)

Abilita o Disabilita la registrazione di debug di una sezione critica specificata.

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

Puntatore a una sezione critica [**CCritSec**](ccritsec.md) .

</dd> <dt>

*fTrace* 
</dt> <dd>

Valore che specifica se la registrazione è abilitata. Usare **true** per abilitare la registrazione o **false** per disabilitarla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare questa funzione per tracciare una sezione critica specifica. Per impostazione predefinita, la registrazione del debug delle sezioni critiche è disabilitata a causa del numero elevato di sezioni critiche.

Per tracciare una sezione critica, seguire questa procedura:

1.  Definire DEBUG o \_ debug prima di includere le intestazioni DirectShow.
2.  Abilitare la registrazione di debug per le sezioni critiche, chiamando [**DbgSetModuleLevel**](dbgsetmodulelevel.md) con il flag di blocco del log \_ .
3.  Chiamare **DbgLockTrace** nella sezione critica che si desidera tracciare.

Nelle compilazioni finali, la funzione **DbgLockTrace** non ha alcun effetto.

## <a name="examples"></a>Esempio

Nell'esempio di codice riportato di seguito viene illustrato come tracciare una sezione critica.


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
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug della sezione critica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




