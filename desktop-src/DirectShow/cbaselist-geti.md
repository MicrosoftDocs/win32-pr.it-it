---
description: Il metodo GetI recupera l'elemento nella posizione specificata.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Metodo CBaseList.GetI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f543a38c3394943e3ccb1eeb8bb97d29297a4ca230966940245a2f8a8c121b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087441"
---
# <a name="cbaselistgeti-method"></a>Metodo CBaseList.GetI

Il `GetI` metodo recupera l'elemento nella posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Indicatore di posizione per l'elemento da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'elemento.

## <a name="remarks"></a>Commenti

Se *pos* è **NULL,** il metodo restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




