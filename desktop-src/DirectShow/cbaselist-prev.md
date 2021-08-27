---
description: Il metodo Prev recupera la posizione precedente nell'elenco.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Metodo CBaseList.Prev (Wxlist.h)
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
ms.openlocfilehash: d04a63079e401b89286e10e927b540f40d04fc186546dbdbd4e31e8610fe617d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076601"
---
# <a name="cbaselistprev-method"></a>Metodo CBaseList.Prev

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

Valore POSITION.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indicatore di posizione precedente alla posizione specificata in *pos*.

## <a name="remarks"></a>Commenti

Se *pos* è la prima posizione nell'elenco, il metodo restituisce **NULL.** Se *pos* è **NULL,** il metodo restituisce l'ultima posizione nell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




