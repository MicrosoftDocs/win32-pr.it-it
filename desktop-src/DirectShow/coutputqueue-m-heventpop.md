---
description: "Evento facoltativo che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda. Il valore è inizialmente NULL. Chiamare il metodo COutputQueue:: SetPopEvent per specificare un handle di evento."
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Membro COutputQueue:: m_hEventPop (Outputq. h)'
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
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327343"
---
# <a name="coutputqueuem_heventpop-member"></a>Membro hEventPop di COutputQueue:: m \_

Evento facoltativo che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda. Il valore è inizialmente **null**. Chiamare il metodo [**COutputQueue:: SetPopEvent**](coutputqueue-setpopevent.md) per specificare un handle di evento.

## <a name="syntax"></a>Sintassi


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




