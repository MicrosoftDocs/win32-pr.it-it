---
description: Il metodo IsValid determina se il filtro è attualmente attivo (in esecuzione o in pausa).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Metodo CBaseFilter. IsValid (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63cf2cd78bb61562c9b4d6a09de3d88c88d4c643
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331541"
---
# <a name="cbasefilterisactive-method"></a>Metodo CBaseFilter. IsValid

Il `IsActive` metodo determina se il filtro è attualmente attivo (in esecuzione o in pausa).

## <a name="syntax"></a>Sintassi


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il filtro è in pausa o in esecuzione oppure **false** se è stato arrestato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




