---
description: Il metodo free viene chiamato durante un'operazione di decommit.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Metodo CMemAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333207"
---
# <a name="cmemallocatorfree-method"></a>CMemAllocator. free, metodo

Il `Free` metodo viene chiamato durante un'operazione di decommit. Questo metodo implementa il metodo [**CBaseAllocator:: Free**](cbaseallocator-free.md) virtuale pure, ma non esegue alcuna operazione. La memoria del buffer non viene effettivamente rilasciata finché l'oggetto **CMemAllocator** non viene eliminato definitivamente. Il metodo del distruttore chiama [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md) per rilasciare la memoria.

## <a name="syntax"></a>Sintassi


```C++
void Free();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




