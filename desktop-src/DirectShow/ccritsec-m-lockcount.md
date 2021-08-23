---
description: Numero di blocchi in sospeso su questo oggetto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: Membro CCritSec::m_lockCount (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9885f3270c021432342605ad84c1b521672022f4a13cecac5ac49c9248c65d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872211"
---
# <a name="ccritsecm_lockcount-member"></a>Membro CCritSec::m \_ lockCount

Numero di blocchi in sospeso su questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro è definita solo nella versione di debug della classe di base. Le [funzioni di debug della sezione critica](critical-section-debugging-functions.md) usano questo membro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




