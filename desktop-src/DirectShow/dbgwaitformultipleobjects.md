---
description: Attende la segnalazione di qualsiasi (o tutti) degli oggetti specificati.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Funzione DbgWaitForMultipleObjects (Wxdebug. h)
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
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333271"
---
# <a name="dbgwaitformultipleobjects-function"></a>DbgWaitForMultipleObjects (funzione)

Attende la segnalazione di qualsiasi (o tutti) degli oggetti specificati.

In una build di debug questa funzione attiva un'asserzione se l'intervallo di timeout scade prima che gli oggetti vengano segnalati. Per impostare l'intervallo di timeout, chiamare la funzione [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

In una build finale questa funzione equivale alla funzione **WaitForMultipleObjects** con un intervallo di timeout infinito.

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

Numero di oggetti.

</dd> <dt>

*lpHandles* 
</dt> <dd>

Matrice di handle per gli oggetti di dimensioni *nCount*.

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valore booleano che specifica se attendere tutti gli oggetti. Se **true**, la funzione attende che tutti gli oggetti vengano segnalati. In caso contrario, attende che venga segnalato almeno un oggetto.

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

 

 




