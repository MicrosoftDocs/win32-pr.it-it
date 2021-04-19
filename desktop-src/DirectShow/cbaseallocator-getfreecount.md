---
description: Il metodo GetFreeCount Recupera il numero di campioni multimediali che non sono in uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Metodo CBaseAllocator. GetFreeCount (Amfilter. h)
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
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331662"
---
# <a name="cbaseallocatorgetfreecount-method"></a>CBaseAllocator. GetFreeCount, metodo

Il `GetFreeCount` metodo recupera il numero di campioni multimediali che non sono in uso.

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

Indirizzo di una variabile che riceve il numero di campioni che non sono in uso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo implementa il metodo [**IMemAllocatorCallbackTemp:: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) . L'allocatore non espone l'interfaccia IMemAllocatorCallbackTemp, a meno che il flag *fEnableReleaseCallback* non sia impostato su **true** nel costruttore CBaseAllocator.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




