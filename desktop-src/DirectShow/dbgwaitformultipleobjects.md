---
description: Attende la segnalazione di uno o tutti gli oggetti specificati.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Funzione DbgWaitForMultipleObjects (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acab4a7f59fe0775e8e474f8a8a2342a5f29ae6266ee36432b0fc1b0e597141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654061"
---
# <a name="dbgwaitformultipleobjects-function"></a>Funzione DbgWaitForMultipleObjects

Attende la segnalazione di uno o tutti gli oggetti specificati.

In una compilazione di debug questa funzione attiva un'asserzione se l'intervallo di timeout scade prima che gli oggetti siano segnalati. Per impostare l'intervallo di timeout, chiamare la [**funzione DbgSetWaitTimeout.**](dbgsetwaittimeout.md)

In una build definitiva questa funzione è equivalente alla **funzione WaitForMultipleObjects** con un intervallo di timeout di INFINITE.

## <a name="syntax"></a>Sintassi


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nCount* 
</dt> <dd>

Numero di oggetti .

</dd> <dt>

*lpHandles* 
</dt> <dd>

Matrice di handle per gli oggetti di dimensioni *nCount.*

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valore booleano che specifica se attendere tutti gli oggetti. Se **TRUE,** la funzione attende la segnalazione di tutti gli oggetti. In caso contrario, attende che almeno un oggetto sia segnalato.

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

 

 




