---
description: Flag per eseguire l'override dell'elaborazione batch. Impostando questo flag su TRUE viene eseguito l'override del flag COutputQueue::m bBatchExact e vengono recapitati \_ tutti gli esempi in sospeso.
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: Membro COutputQueue::m_bSendAnyway (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c01ec87fb8e1d9b33fd88806b0d2798e2b13e76eea2ec47b4e1766a7e10201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954150"
---
# <a name="coutputqueuem_bsendanyway-member"></a>Membro COutputQueue::m \_ bSendAnyway

Flag per eseguire l'override dell'elaborazione batch. Impostando questo flag su **TRUE** viene eseguito l'override del flag [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) e vengono recapitati tutti gli esempi in sospeso.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




