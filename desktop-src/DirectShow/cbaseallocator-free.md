---
description: Il metodo Free rilascia tutta la memoria del buffer. Questo metodo viene chiamato quando il filtro proprietario esegue il commit dell'allocatore, dopo il rilascio dell'ultimo campione multimediale.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Metodo CBaseAllocator. Free (Amfilter. h)
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
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328268"
---
# <a name="cbaseallocatorfree-method"></a>CBaseAllocator. free, metodo

Il `Free` metodo rilascia tutta la memoria del buffer. Questo metodo viene chiamato quando il filtro proprietario esegue il commit dell'allocatore, dopo il rilascio dell'ultimo campione multimediale.

## <a name="syntax"></a>Sintassi


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Dopo la chiamata del metodo [**decommit**](cbaseallocator-decommit.md) , l'allocatore chiama questo metodo quando rilascia l'ultimo esempio di supporto. La classe derivata deve implementare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




