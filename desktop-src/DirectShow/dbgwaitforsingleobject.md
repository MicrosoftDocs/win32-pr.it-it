---
description: Attende che un oggetto diventi segnalato.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Funzione DbgWaitForSingleObject (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749351"
---
# <a name="dbgwaitforsingleobject-function"></a>Funzione DbgWaitForSingleObject

Attende che un oggetto diventi segnalato.

In una compilazione di debug questa funzione attiva un'asserzione se l'intervallo di timeout scade prima che l'oggetto venga segnalato. Per impostare l'intervallo di timeout, chiamare la [**funzione DbgSetWaitTimeout.**](dbgsetwaittimeout.md)

In una build definitiva questa funzione è equivalente alla **funzione WaitForSingleObject** con un intervallo di timeout di INFINITE.

## <a name="syntax"></a>Sintassi


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*h* 
</dt> <dd>

Handle per l'oggetto .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug wait](wait-debugging-functions.md)
</dt> </dl>

 

 




