---
description: Il metodo di decommit consente di eseguire il commit dell'allocatore. Questo metodo implementa il metodo IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Metodo CBaseAllocator. decommit (Amfilter. h)
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
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328270"
---
# <a name="cbaseallocatordecommit-method"></a>CBaseAllocator. decommit (metodo)

Il `Decommit` metodo consente di eseguire il commit dell'allocatore. Questo metodo implementa il metodo [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Dopo la chiamata a questo metodo, le chiamate al metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) avranno esito negativo. Man mano che vengono rilasciati, gli esempi vengono restituiti all'elenco di disponibilità. Quando viene restituito l'ultimo esempio, l'allocatore chiama il metodo [**CBaseAllocator:: Free**](cbaseallocator-free.md) , che rilascia la memoria allocata. Nella classe di base, **Free** è un metodo virtuale puro.

Questo metodo rilascia inoltre tutti i thread bloccati sulle chiamate a **GetBuffer** . Le chiamate a **GetBuffer** hanno esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




