---
description: La funzione DbgTerminate pulisce la libreria di debug. Ignorato nelle build di vendita al dettaglio.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Funzione DbgTerminate (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6846f6899730a8b9d128d1bc0a6069fd8a67a5f4f9d8a5a3d618bebad67b0468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821567"
---
# <a name="dbgterminate-function"></a>Funzione DbgTerminate

La **funzione DbgTerminate** pulisce la libreria di debug. Ignorato nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Chiamare questa funzione se si chiama la [**funzione DbgInitialise.**](dbginitialise.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




