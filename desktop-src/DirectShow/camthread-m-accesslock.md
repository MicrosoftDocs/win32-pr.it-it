---
description: Sezione critica che blocca l'accesso al thread da parte di altri thread.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Membro CAMThread:: m_AccessLock (Wxutil. h)'
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
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330703"
---
# <a name="camthreadm_accesslock-member"></a>Membro AccessLock di CAMThread:: m \_

Sezione critica che blocca l'accesso al thread da parte di altri thread.

## <a name="syntax"></a>Sintassi


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Osservazioni

I metodi [**CAMThread:: create**](camthread-create.md) e [**CAMThread:: CallWorker**](camthread-callworker.md) mantengono questo blocco per serializzare le operazioni sul thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




