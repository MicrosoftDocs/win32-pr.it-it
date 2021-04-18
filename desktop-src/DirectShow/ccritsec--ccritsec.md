---
description: Metodo del distruttore.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Distruttore CCritSec. ~ CCritSec (Wxutil. h)
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
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330858"
---
# <a name="ccritsecccritsec-destructor"></a>Distruttore CCritSec. ~ CCritSec

Metodo del distruttore.

## <a name="syntax"></a>Sintassi


```C++
~CCritSec();
```



## <a name="remarks"></a>Osservazioni

Questo metodo chiama la funzione [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) per eliminare la sezione critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

