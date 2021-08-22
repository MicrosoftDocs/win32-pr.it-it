---
description: Il metodo Decommit disacconto l'allocatore. Questo metodo implementa il metodo IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Metodo CBaseAllocator.Decommit (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 614986a912f08d918d4fbbaf6b3eeeb0d3b2c3eabc47748351934a08b8280cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017549"
---
# <a name="cbaseallocatordecommit-method"></a>Metodo CBaseAllocator.Decommit

Il `Decommit` metodo disaccommia l'allocatore. Questo metodo implementa il [**metodo IMemAllocator::D ecommit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Dopo la chiamata di questo metodo, le chiamate al [**metodo CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) avranno esito negativo. Man mano che vengono rilasciati, gli esempi vengono restituiti all'elenco gratuito. Quando viene restituito l'ultimo esempio, l'allocatore chiama il [**metodo CBaseAllocator::Free,**](cbaseallocator-free.md) che rilascia la memoria allocata. Nella classe di base **Free è** un metodo virtuale puro.

Inoltre, questo metodo rilascia tutti i thread bloccati nelle **chiamate GetBuffer.** Le chiamate a **GetBuffer hanno esito** negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




