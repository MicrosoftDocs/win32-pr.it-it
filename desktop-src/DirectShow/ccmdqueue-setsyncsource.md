---
description: Il metodo SetSyncSource imposta l'orologio usato per l'intervallo.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Metodo CCmdQueue.SetSyncSource (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3877fb52a1e2268d24974ee3575c712d27a107f4429398ada9de1ebf5e728675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757151"
---
# <a name="ccmdqueuesetsyncsource-method"></a>Metodo CCmdQueue.SetSyncSource

Il `SetSyncSource` metodo imposta l'orologio usato per l'intervallo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIrc* 
</dt> <dd>

Puntatore [**all'interfaccia IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




