---
description: Il metodo AddHeadI aggiunge un elemento all'inizio dell'elenco.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Metodo CBaseList.AddHeadI (Wxlist.h)
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
ms.openlocfilehash: 4c1f22434aa2c927933c36ec496d5880ca8f3f673b314d7a8197079203757427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568121"
---
# <a name="cbaselistaddheadi-method"></a>Metodo CBaseList.AddHeadI

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

Restituisce un valore POSITION che indica la nuova posizione della testa.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, il valore restituito è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




