---
description: Il metodo AddTailI aggiunge un elemento alla fine dell'elenco.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Metodo CBaseList.AddTailI (Wxlist.h)
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
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659127"
---
# <a name="cbaselistaddtaili-method"></a>Metodo CBaseList.AddTailI

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

Restituisce un valore POSITION per la nuova posizione della coda.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




