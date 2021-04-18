---
description: Il metodo AddBeforeI inserisce un elemento prima della posizione specificata.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Metodo CBaseList. AddBeforeI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328678"
---
# <a name="cbaselistaddbeforei-method"></a>CBaseList. AddBeforeI, metodo

Il `AddBeforeI` metodo inserisce un elemento prima della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Posizione prima della quale aggiungere l'elemento.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntatore all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione per l'elemento inserito.

## <a name="remarks"></a>Commenti

Se *pos* è **null**, questo metodo aggiunge l'elemento alla parte finale dell'elenco (equivalente alla chiamata al metodo [**CBaseList:: AddTailI**](cbaselist-addtaili.md) ).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




