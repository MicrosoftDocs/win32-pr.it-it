---
description: Distruttore CCritSec.~CCritSec - Metodo distruttore.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Distruttore CCritSec.~CCritSec (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d34665bb18a6ea9f6e76ad6332a5d7f344993067848c1b5e473893e702b62a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999611"
---
# <a name="ccritsecccritsec-destructor"></a>Distruttore CCritSec.~CCritSec

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CCritSec();
```



## <a name="remarks"></a>Osservazioni

Questo metodo chiama la [**funzione DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) per eliminare la sezione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

