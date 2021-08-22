---
description: Il metodo Unlock sblocca l'oggetto sezione critica.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Metodo CCritSec.Unlock (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 919b73e5e1fc0becfb7c5fad40b87a5eb28fa008ba5cea1706373ddec9128682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074385"
---
# <a name="ccritsecunlock-method"></a>Metodo CCritSec.Unlock

Il **metodo Unlock** sblocca l'oggetto sezione critica.

## <a name="syntax"></a>Sintassi


```C++
void Unlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo chiama la [**funzione LeaveCriticalSection.**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) Chiamare questo metodo una volta per ogni chiamata al [**metodo CCritSec::Lock.**](ccritsec-lock.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

