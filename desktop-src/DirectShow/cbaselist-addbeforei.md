---
description: Il metodo AddBeforeI inserisce un elemento prima della posizione specificata.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Metodo CBaseList.AddBeforeI (Wxlist.h)
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
ms.openlocfilehash: cfb995e614904e807e67eeee9c0f344525fd701d039c596eb081b6ff3be4f078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823748"
---
# <a name="cbaselistaddbeforei-method"></a>Metodo CBaseList.AddBeforeI

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

Se *pos* è **NULL,** questo metodo aggiunge l'elemento alla parte finale dell'elenco (equivalente alla chiamata del metodo [**CBaseList::AddTailI).**](cbaselist-addtaili.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




