---
description: Sezione critica che blocca l'accesso al thread da parte di altri thread.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: Membro CAMThread::m_AccessLock (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017599"
---
# <a name="camthreadm_accesslock-member"></a>Membro CAMThread::m \_ AccessLock

Sezione critica che blocca l'accesso al thread da parte di altri thread.

## <a name="syntax"></a>Sintassi


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Osservazioni

I [**metodi CAMThread::Create**](camthread-create.md) e [**CAMThread::CallWorker**](camthread-callworker.md) mantendono questo blocco per serializzare le operazioni sul thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




