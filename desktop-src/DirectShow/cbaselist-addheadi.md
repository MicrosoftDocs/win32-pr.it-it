---
description: Il metodo AddHeadI aggiunge un elemento all'inizio dell'elenco.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Metodo CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328673"
---
# <a name="cbaselistaddheadi-method"></a>CBaseList. AddHeadI, metodo

Il `AddHeadI` metodo aggiunge un elemento all'inizio dell'elenco.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddHeadI(
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

Restituisce un valore di posizione che indica la nuova posizione Head.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, il valore restituito è **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




