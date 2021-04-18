---
description: Il metodo AddAfterI inserisce un elemento dopo la posizione specificata.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Metodo CBaseList. AddAfterI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328684"
---
# <a name="cbaselistaddafteri-method"></a>CBaseList. AddAfterI, metodo

Il `AddAfterI` metodo inserisce un elemento dopo la posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Posizione dopo la quale aggiungere l'elemento.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntatore all'elemento da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione dell'elemento inserito.

## <a name="remarks"></a>Commenti

Se *pos* è **null**, questo metodo aggiunge l'elemento all'inizio dell'elenco (equivalente alla chiamata al metodo [**CBaseList:: AddHeadI**](cbaselist-addheadi.md) ).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




