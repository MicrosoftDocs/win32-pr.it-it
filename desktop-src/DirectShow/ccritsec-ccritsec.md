---
description: 'Costruttore CCritSec.CCritSec : metodo del costruttore.'
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Costruttore CCritSec.CCritSec (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fce4cb5edb9765e7f69726188e5ed0ba2017df7d6fa90cae0bfa059b89fc939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688991"
---
# <a name="ccritsecccritsec-constructor"></a>Costruttore CCritSec.CCritSec

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CCritSec();
```



## <a name="parameters"></a>Parametri

Questo costruttore non ha parametri.

## <a name="remarks"></a>Commenti

Questo metodo chiama la [**funzione InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) per inizializzare la sezione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

