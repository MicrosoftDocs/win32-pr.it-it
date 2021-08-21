---
description: Valore booleano che specifica se tracciare questo blocco.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: Membro CCritSec::m_fTrace (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5a47437e4f9ab475b64979ec970604ac7a621d2ab53ea7a3c87742fa81a8aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074395"
---
# <a name="ccritsecm_ftrace-member"></a>Membro fTrace CCritSec::m \_

Valore booleano che specifica se tracciare questo blocco.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro è definita solo nella versione di debug della classe di base. Se il valore è **TRUE,** nel log di debug viene scritta una traccia dello stato di blocco. La registrazione di debug per le sezioni critiche deve essere attiva. Per altre informazioni, vedere [**DbgLockTrace.**](dbglocktrace.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




