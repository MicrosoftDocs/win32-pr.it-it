---
description: Il metodo EndFlush termina un'operazione di scaricamento. Questo metodo esegue l'override del metodo CTransformFilter::EndFlush.
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Metodo CVideoTransformFilter.EndFlush (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359229e690715667d7bbfbe3d3a9134f41f5af9febc185885e08cde7d986896e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155875"
---
# <a name="cvideotransformfilterendflush-method"></a>Metodo CVideoTransformFilter.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento. Questo metodo esegue l'override del metodo [**CTransformFilter::EndFlush.**](ctransformfilter-endflush.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o un codice di errore.

## <a name="remarks"></a>Commenti

Questo metodo reimposta tutte le misurazioni delle prestazioni interne del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




