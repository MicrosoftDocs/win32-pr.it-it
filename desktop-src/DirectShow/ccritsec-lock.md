---
description: Il metodo Lock blocca l'oggetto sezione critica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Metodo CCritSec.Lock (Wxutil.h)
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
ms.openlocfilehash: 4241b2cd5e94fbd6a3cbe0abd91d47ad6312c44b71f76c214cffb22836033a7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928590"
---
# <a name="ccritseclock-method"></a>Metodo CCritSec.Lock

Il **metodo Lock** blocca l'oggetto sezione critica.

## <a name="syntax"></a>Sintassi


```C++
void Lock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo chiama la [**funzione EnterCriticalSection.**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection)

Chiamare la [**funzione membro CCritSec::Unlock**](ccritsec-unlock.md) per sbloccare la sezione critica. È possibile effettuare più chiamate al **metodo Lock** nello stesso thread. Assicurarsi di chiamare **Unlock** un numero corrispondente di volte.

Se l'oggetto è già bloccato da un altro thread, il metodo **CCritSec::Lock** si blocca fino al rilascio dell'oggetto o fino a quando non si verifica una possibile eccezione deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

