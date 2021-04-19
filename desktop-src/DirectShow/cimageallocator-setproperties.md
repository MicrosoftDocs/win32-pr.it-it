---
description: "Il metodo seproperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo esegue l'override del metodo CBaseAllocator:: SetValue."
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Metodo CImageAllocator. seproperties (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331789"
---
# <a name="cimageallocatorsetproperties-method"></a>Metodo CImageAllocator. seproperties

Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo esegue l'override del metodo [**CBaseAllocator::**](cbaseallocator-setproperties.md) SetValue.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRequest* 
</dt> <dd>

Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntatore a una struttura di **\_ proprietà dell'allocatore** che riceve le proprietà effettive del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo chiama [**CImageAllocator:: CheckSizes**](cimageallocator-checksizes.md) per convalidare le dimensioni del buffer richieste. Viene anche chiamata la versione della classe di base di `SetProperties` .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




