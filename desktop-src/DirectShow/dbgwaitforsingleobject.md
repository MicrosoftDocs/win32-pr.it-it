---
description: Attende che un oggetto venga segnalato.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Funzione DbgWaitForSingleObject (Wxdebug. h)
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
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333268"
---
# <a name="dbgwaitforsingleobject-function"></a>DbgWaitForSingleObject (funzione)

Attende che un oggetto venga segnalato.

In una build di debug questa funzione attiva un'asserzione se l'intervallo di timeout scade prima che l'oggetto venga segnalato. Per impostare l'intervallo di timeout, chiamare la funzione [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

In una build finale questa funzione equivale alla funzione **WaitForSingleObject** con un intervallo di timeout infinito.

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

Handle per l'oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di debug di attesa](wait-debugging-functions.md)
</dt> </dl>

 

 




