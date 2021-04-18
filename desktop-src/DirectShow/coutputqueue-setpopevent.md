---
description: Il metodo SetPopEvent specifica un evento che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Metodo COutputQueue. SetPopEvent (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324670"
---
# <a name="coutputqueuesetpopevent-method"></a>COutputQueue. SetPopEvent, metodo

Il `SetPopEvent` metodo specifica un evento che viene segnalato ogni volta che l'oggetto rimuove un campione dalla coda.

## <a name="syntax"></a>Sintassi


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* 
</dt> <dd>

Handle per un evento creato dal chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




