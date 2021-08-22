---
description: Identificatore di thread del thread proprietario.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: Membro CCritSec::m_currentOwner (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71c88055f5068a5486c1eb6e3ac739235a6b7cde2e8d6b767380160ff12503be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657214"
---
# <a name="ccritsecm_currentowner-member"></a>Membro CCritSec::m \_ currentOwner

Identificatore di thread del thread proprietario.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_currentOwner;
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

 

 




