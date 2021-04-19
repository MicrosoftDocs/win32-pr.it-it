---
description: "Il metodo GetProperties Recupera il numero di buffer che l'allocatore creerà e le proprietà del buffer. Questo metodo implementa il metodo IMemAllocator:: GetProperties."
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Metodo CBaseAllocator. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328174"
---
# <a name="cbaseallocatorgetproperties-method"></a>Metodo CBaseAllocator. GetProperties

Il `GetProperties` metodo recupera il numero di buffer che l'allocatore creerà e le proprietà del buffer. Questo metodo implementa il metodo [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProps* 
</dt> <dd>

Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che riceve le proprietà dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




