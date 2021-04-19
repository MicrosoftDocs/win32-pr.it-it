---
description: Imposta il valore di timeout del debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Funzione DbgSetWaitTimeout (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326660"
---
# <a name="dbgsetwaittimeout-function"></a>DbgSetWaitTimeout (funzione)

Imposta il valore di timeout del debug. Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valore di timeout in millisecondi o infinito per un'attesa indefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug, le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usano questo valore come intervallo di timeout.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug di attesa](wait-debugging-functions.md)
</dt> </dl>

 

 




