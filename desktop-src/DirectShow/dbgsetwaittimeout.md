---
description: Imposta il valore di timeout del debug. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Funzione DbgSetWaitTimeout (Wxdebug.h)
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
ms.openlocfilehash: 67a5522184b9e88cd4b8ac9f23246f96c13ffad2175d625334de32d34c750e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654023"
---
# <a name="dbgsetwaittimeout-function"></a>Funzione DbgSetWaitTimeout

Imposta il valore di timeout del debug. Ignorato nelle build per la vendita al dettaglio.

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

Valore di timeout in millisecondi o INFINITE per un'attesa illimitata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usano questo valore come intervallo di timeout.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug wait](wait-debugging-functions.md)
</dt> </dl>

 

 




