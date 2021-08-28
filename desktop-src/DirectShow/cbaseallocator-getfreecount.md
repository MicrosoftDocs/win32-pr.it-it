---
description: Il metodo GetFreeCount recupera il numero di campioni di supporti non in uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Metodo CBaseAllocator.GetFreeCount (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c4552829482a604b368a6710c62d0fc0b26a94aa3bb33b67ef386f2785d6c90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057511"
---
# <a name="cbaseallocatorgetfreecount-method"></a>Metodo CBaseAllocator.GetFreeCount

Il `GetFreeCount` metodo recupera il numero di campioni di supporti non in uso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plBuffersFree* 
</dt> <dd>

Indirizzo di una variabile che riceve il numero di campioni non in uso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo implementa il [**metodo IMemAllocatorCallbackTemp::GetFreeCount.**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) L'allocatore non espone l'interfaccia IMemAllocatorCallbackTemp a meno che il flag *fEnableReleaseCallback* non sia impostato su **TRUE** nel costruttore CBaseAllocator.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




