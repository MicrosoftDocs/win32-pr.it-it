---
description: Il metodo Free rilascia tutta la memoria del buffer. Questo metodo viene chiamato quando il filtro proprietario decommita l'allocatore, dopo il rilascio dell'ultimo campione multimediale.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Metodo CBaseAllocator.Free (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77555094625bfc6a31a0527fc3223a124b012e72c28ea76e5774de289d63391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794211"
---
# <a name="cbaseallocatorfree-method"></a>Metodo CBaseAllocator.Free

Il `Free` metodo rilascia tutta la memoria del buffer. Questo metodo viene chiamato quando il filtro proprietario decommita l'allocatore, dopo il rilascio dell'ultimo campione multimediale.

## <a name="syntax"></a>Sintassi


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Dopo aver [**chiamato il metodo Decommit,**](cbaseallocator-decommit.md) l'allocatore chiama questo metodo quando rilascia l'ultimo campione multimediale. La classe derivata deve implementare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




