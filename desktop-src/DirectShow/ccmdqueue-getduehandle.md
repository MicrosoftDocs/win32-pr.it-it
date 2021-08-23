---
description: Il metodo GetDueHandle recupera l'handle di evento da segnalare.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Metodo CCmdQueue.GetDueHandle (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62fbe0e38e24891add93e63e0c03d521289ed345078e8e567a376e9bd639d997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016419"
---
# <a name="ccmdqueuegetduehandle-method"></a>Metodo CCmdQueue.GetDueHandle

Il `GetDueHandle` metodo recupera l'handle dell'evento da segnalare.

## <a name="syntax"></a>Sintassi


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce l'handle dell'evento.

## <a name="remarks"></a>Commenti

Restituisce l'handle dell'evento ogni volta che sono presenti comandi posticilati per l'esecuzione (quando [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) non si blocca).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




