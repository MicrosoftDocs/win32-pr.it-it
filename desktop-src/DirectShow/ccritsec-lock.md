---
description: Il metodo Lock blocca l'oggetto sezione critica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Metodo CCritSec. Lock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333732"
---
# <a name="ccritseclock-method"></a>Metodo CCritSec. Lock

Il metodo **Lock** blocca l'oggetto sezione critica.

## <a name="syntax"></a>Sintassi


```C++
void Lock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo chiama la funzione [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .

Chiamare la funzione membro [**CCritSec:: Unlock**](ccritsec-unlock.md) per sbloccare la sezione critica. È possibile eseguire più chiamate al metodo **Lock** sullo stesso thread. Assicurarsi di chiamare **Unlock** un numero di volte corrispondente.

Se l'oggetto è già bloccato da un altro thread, il metodo **CCritSec:: Lock** si blocca fino a quando l'oggetto non viene rilasciato o fino a quando non si verifica un'eccezione di deadlock possibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

