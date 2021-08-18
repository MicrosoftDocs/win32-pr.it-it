---
description: Il metodo pStateLock recupera un puntatore all'oggetto sezione critica del filtro.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Metodo CSource.pStateLock (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b74027e2ee2339e647938592e05162ce85108eb6985061b30a825394c2f2e7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953790"
---
# <a name="csourcepstatelock-method"></a>Metodo CSource.pStateLock

Il **metodo pStateLock** recupera un puntatore all'oggetto sezione critica del filtro.

> [!Note]  
> Anche se denominato come una variabile membro, **pStateLock** è un metodo.

 

## <a name="syntax"></a>Sintassi


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore alla [**variabile membro \_ cStateLock CSource::m.**](csource-m-cstatelock.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




