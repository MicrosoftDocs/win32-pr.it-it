---
description: Puntatore a un oggetto sezione critica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: Membro CSourceSeeking::m_pLock (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f230fcaee4ebb59520319d5dfd7cf8295ce8721716cd1ffb02b534e242bd99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054021"
---
# <a name="csourceseekingm_plock-member"></a>Membro PLock CSourceSeeking::m \_

Puntatore a un oggetto sezione critica. La classe usa questa sezione critica per sincronizzare l'accesso alle variabili di ora di inizio e `CSourceSeeking` arresto, durata e frequenza. Questa variabile viene inizializzata nel metodo del costruttore. vedere [**CSourceSeeking::CSourceSeeking.**](csourceseeking-csourceseeking.md)

## <a name="syntax"></a>Sintassi


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




