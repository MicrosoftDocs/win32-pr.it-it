---
description: Il metodo Prev recupera la posizione precedente nell'elenco.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Metodo CBaseList. prev (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328644"
---
# <a name="cbaselistprev-method"></a>CBaseList. prev, metodo

Il `Prev` metodo recupera la posizione precedente nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Valore della posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione precedente alla posizione specificata in *pos*.

## <a name="remarks"></a>Commenti

Se *pos* è la prima posizione nell'elenco, il metodo restituisce **null**. Se *pos* è **null**, il metodo restituisce l'ultima posizione nell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




