---
description: Recupera l'handle per il thread nell'oggetto CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Metodo CMsgThread.GetThreadHandle (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ecb968156302c4fd1a8c48d1c6f3175977059298d2f6af5207abc376a6e107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585691"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>Metodo CMsgThread.GetThreadHandle

Recupera l'handle per il thread [**nell'oggetto CMsgThread.**](cmsgthread.md)

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce l'handle del thread.

## <a name="remarks"></a>Commenti

L'handle del thread può essere passato alle funzioni di attesa, ad [**esempio WaitForMultipleObjects.**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) L'handle del thread viene segnalato quando il thread è terminato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

