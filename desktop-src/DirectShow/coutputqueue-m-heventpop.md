---
description: Evento facoltativo segnalato ogni volta che l'oggetto rimuove un campione dalla coda. Il valore è inizialmente NULL. Chiamare il metodo COutputQueue::SetPopEvent per specificare un handle di evento.
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: Membro COutputQueue::m_hEventPop (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb401cf9755260c797ebfb382d9f2248d9d04c5f8d9e9b49e319c390de1664c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087211"
---
# <a name="coutputqueuem_heventpop-member"></a>Membro COutputQueue::m \_ hEventPop

Evento facoltativo segnalato ogni volta che l'oggetto rimuove un campione dalla coda. Il valore è inizialmente **NULL.** Chiamare il [**metodo COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) per specificare un handle di evento.

## <a name="syntax"></a>Sintassi


```C++
HANDLE m_hEventPop;
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

 

 




