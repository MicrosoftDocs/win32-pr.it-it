---
description: Il metodo AddTailI aggiunge un elemento alla fine dell'elenco.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Metodo CBaseList. AddTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330702"
---
# <a name="cbaselistaddtaili-method"></a>CBaseList. AddTailI, metodo

Il `AddTailI` metodo aggiunge un elemento alla fine dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObj* 
</dt> <dd>

Puntatore all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore di posizione per la nuova posizione della coda.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




