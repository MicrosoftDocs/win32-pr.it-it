---
description: Il metodo AddAfterI inserisce un elemento dopo la posizione specificata.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Metodo CBaseList.AddAfterI (Wxlist.h)
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
ms.openlocfilehash: b72be7342e6085b773ef2493f5ad138f73349dffcdafc1a60a380692df3f16ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016989"
---
# <a name="cbaselistaddafteri-method"></a>Metodo CBaseList.AddAfterI

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

Se *pos* è **NULL,** questo metodo aggiunge l'elemento all'intestazione dell'elenco (equivalente a chiamare il metodo [**CBaseList::AddHeadI).**](cbaselist-addheadi.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




