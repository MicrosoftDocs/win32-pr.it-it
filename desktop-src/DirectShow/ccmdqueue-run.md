---
description: Il metodo Run passa alla modalità di esecuzione in modo che sia possibile eseguire i comandi rinviati dall'ora del flusso.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Metodo CCmdQueue. Run (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324472"
---
# <a name="ccmdqueuerun-method"></a>Metodo CCmdQueue. Run

Il `Run` metodo passa alla modalità di esecuzione in modo che sia possibile eseguire i comandi rinviati dall'ora del flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

Tempo di offset.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

In modalità di esecuzione, è noto il mapping del flusso di tempo per presentazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




